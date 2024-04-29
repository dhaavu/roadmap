<template>
<div class="container">
    <div class="card">
        <div class="title">
            <h1>
                Digital Marketing 
            </h1>
            <div class="itmes">
                <div class="item">
                    <div class="itemTitle">
                        Customer Personalization and Segmentation.
                    </div>
                    <div class="yearContainer">
                    <div class="year y2024">
                        
                    </div>
                    <div class="year y2025">

                    </div>
                    <div class="year y2026">

                    </div>
                    </div>
                    
                </div>
            </div>
        </div>
    </div>
</div>

</template>



<style scoped>

.container
{
    margin: 0 auto;
}
.card{
    border: 1px solid rgb(208, 208, 208);
    box-shadow:3px 3px 5px 6px #ccc; 
    background: #0055ff1e;
    margin:10px; 
}
.title{
    text-align: center;
}
.item{
    background: #0000ff10;
    color:rgb(11, 11, 11); 
    padding:10px; 
    display: flex;
    justify-content: space-between;
    margin: 20px;
}
.year{
   
    min-width: 10px;
    background:red; 
    margin:3px; 
}
.yearContainer{
    display: flex;
}
.y2024{
 background:blue
}
.y2025{
 background:rgb(255, 136, 0)
}
.y2026{
 background:rgb(0, 255, 200)
}
</style>

<script>
import * as XLSX from "sheetjs";

export default {
    methods: {
  async handleFileUpload(event) {
    const file = event.target.files[0];

    if (!file) return;

    const reader = new FileReader();
    reader.onload = (e) => {
      const arrayBuffer = e.target.result;
      const data = this.parseExcelData(arrayBuffer);
      // Do something with the parsed data (e.g., assign it to a variable)
    };
    reader.readAsArrayBuffer(file);
  },
  parseExcelData(arrayBuffer) {
    const wb = XLSX.read(arrayBuffer);
    const sheetName = wb.SheetNames[0];
    const sheetData = XLSX.utils.sheet_to_json(wb.Sheets[sheetName]);
    return sheetData;
  },
},

}
</script>