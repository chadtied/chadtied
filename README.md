const XLSX= require("xlsx");
const workbook= XLSX.readFile("taiwan.xlsx");

let worksheet= {};

for(const sheetName of workbook.SheetNames){
    worksheet[sheetName]= XLSX.utils.sheet_to_json(workbook.Sheets[sheetName]);
}
var a= worksheet["工作表1"][1]['公司'];
console.log(typeof(a));
