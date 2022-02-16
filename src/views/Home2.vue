<template>
 <div>
  <div>
      <p>Hello World !!!</p>
      <body style="background-color: wheat;" >
    <div id="table_">
        <div style="text-align: center; margin-top: 20px;">

            <form action="">
                <label for="">To do</label>
                <input type="text" v-model="do_">
              

            </form>

            <button v-on:click="addData()"> Submit </button>





        </div>


          <div  class="container mt-3">
            <table  class="table table-striped">
                <thead>
                    <tr>
                      <th>To Do</th>
                      <th>   delete </th>
                     
                     
                    </tr>
                  </thead>
                <tr v-for="(stu,index) in doList" :key="index">
                    
                    <td style="  height: 60px; font-size= 150% ; color:blue;">{{stu}}</td>
                    
                    <td> <button @click="deleteData()" > delete  </button></td>
                </tr>
            </table>



          </div>

    </div>
   

 


</body>

  
  
  
  </div>
  </div>


</template>

<script>
export default {
    data: () =>({
    counter: 0,
    do_:""
    ,
    
    doList :[]
  }),
  methods: {

    addData:function () {

       
      
       

        this.doList.push(this.do_);
        console.log(this.doList);
        console.log(this.do_);
        
         
    

      

    },

    deleteData :function() {
      this.doList.pop();
      


    }

    

      
  }
};
</script>

<style>
.mt-3 
{
  margin: 0px;
  border: 1px solid black;
  


}

</style>
