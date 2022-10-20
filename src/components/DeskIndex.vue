<template>
    <div>
      <div class="main">
         <div class="header">
            <el-input v-model="input" 
            placeholder="请输入内容" 
            @keyup.enter.native="search"
            >
               <i slot="suffix" class="el-icon-search el-input__icon" @click="search"></i>
            </el-input>
         </div>
         <div class="footer">
            <span class="iconfont icon-baidu" @click="moveTo('baidu')"></span>
            <span class="iconfont icon-zhihu" @click="moveTo('zhihu')"></span>
            <span class="iconfont icon-github-fill" @click="moveTo('github')"></span>
            <span class="iconfont icon-Bing" @click="moveTo('bing')"></span>
         </div>
      </div>
    </div>
</template>
<script>
export default {
   data() {
      return {
         input:""
      }
   },
   created(){
   },
   computed:{
   },
   methods:{
      suggest(){
         
      },
      search(){
         window.open("https://www.bing.com/search?q="+this.input);
      },
      moveTo(item){
         window.open("http://www."+item+".com")
      }
   }
}
</script>
<style  scoped>
.main {
   display: flex;
   justify-content: center;
   align-items: center;
   flex-direction: column;
}

.header {
   width: 40vw;
   height: 30vh;
   display: flex;
   justify-content: flex-end;
   align-items: center;
   flex-direction: column;
}
@media screen and (max-width:800px)  {
   .header {
      width: 80vw;
   }
}
.footer {
   box-sizing: border-box;
   padding-top: 100px;
   width: 40vw;
   height: 70vh;
   display: flex;
   justify-content: center;
   align-items:flex-start;
   flex-direction: row;
}
.footer span {
   display: inline-block;
   border-radius: 10px;
   background-color: white;
   position: relative;
   bottom: 0;
   width: 40px;
   aspect-ratio: 1/1;
   margin: 0 30px;
   transition: .7s;
}
.footer span::before{
   position: absolute;
   top: 50%;
   left: 50%;
   transform: translate(-50%,-50%);
   font-size: 26px;
}
.footer span:hover {
   position: relative;
   bottom: 10px;
   background-color: #DCDCDC;
}
</style>
