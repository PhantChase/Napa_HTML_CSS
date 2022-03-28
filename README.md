# Excercise

### BT1. Thêm code ở dưới làm sao để "Hello!!!" in ra sau 4 giây
```
setTimeout(() => { console.log('Hello!!!'); }, 1000);
// Code here
```
Sold:
```
setTimeout(() => {  
	console.log('Hello!!!');  
}, 1000);  
  
let startDate = new Date().getTime();  
let endDate = startDate;  
  
while (endDate < startDate + 3000) {  
	endDate = new Date().getTime();  
}
```

### BT2. Viết xử lý lặp qua toàn bộ folder, lấy nội dung trong file1.txt và file2.txt ở mỗi folder, sau đó cộng lại và in ra màn hình
#### FOR
```
const fs = require("fs");

function getPath(index, filename) {
  let path = __dirname + "/" + index + "/" + filename + ".txt";
  return path;
}

function sleep(ms) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}

async function getAllFile() {
  let sum = 0;
  for (let i = 0; i < 10; i++) {
    await sleep(1000).then(() => {
      return new Promise((resolve) => {
        
        const content1 = fs.readFileSync(getPath(i + 1, "file1"), "utf-8");
        const content2 = fs.readFileSync(getPath(i + 1, "file2"), "utf-8");
        numberA = i+parseInt(1)
        sumText = parseInt(content1) + parseInt(content2)
        console.log("Folder " + numberA )
        console.log("Số ở File 1 : " + content1 )
        console.log("Số ở File 2 : " + content2 )
        console.log("Tổng ở Folder " + numberA + " là: " + sumText)
        resolve(Number(content1) + Number(content2));
        sum += Number(content1) + Number(content2);
      });
    });
  }
  console.log("Tổng toàn bộ số trong toàn bộ folder: " + sum);
}

getAllFile();
```
#### MAP
```
const fs = require("fs");

function sleep(ms, index) {
  return new Promise((resolve) => setTimeout(resolve, ms * index));
}

function getPath(index, filename) {
  let path = __dirname + "\\folder\\" + index + "\\" + filename + ".txt";
  return path;
}

const list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const getContent = async () => {
  let sum = 0;
  list.map(async (i, index) => {
    await sleep(1000, index + 1).then(() => {
      return new Promise((resolve) => {
        const content1 = fs.readFileSync(getPath(i, "file1"), "utf-8");
        const content2 = fs.readFileSync(getPath(i, "file2"), "utf-8");
        var numberA = i+parseInt(1);
        var sumText = parseInt(content1) + parseInt(content2);
        console.log("Folder " + numberA )
        console.log("Số ở File 1 : " + content1 )
        console.log("Số ở File 2 : " + content2 )
        console.log("Tổng ở Folder " + numberA + " là: " + sumText)
        resolve(Number(content1) + Number(content2));
        sum += Number(content1) + Number(content2);
      });
    });
  });
  sleep(1000, 10).then(() => console.log("Tổng toàn bộ số trong toàn bộ folder: " + sum));
};

getContent();
```


### BT3. Clone Sidebar from thi site (https://antd-admin.zuiidea.com/)
Screen shot:
![](https://uphinh.vn/images/2022/03/23/c59a84e45e660721542fd9fb5567b636.png)

Check this link : [([Side bar (phantchase.github.io)](https://phantchase.github.io/napa/))

### BT4. Phân biệt let, var, const trong javascript

 # | Var | Let | Const | 
--- | --- | --- | --- |
Cập nhật | ✔ | ✔ | ❌ |
Khai báo lại | ✔ | ❌ | ❌ |

### BT5. Phân biệt tham chiếu, tham trị

#### Tham trị
```
let a = 1;
//Tạo ra biến a và lưu giá trị của a vào ô nhớ - 1

let b = a;
//Tạo ra biến b, sao chép giá trị của biến a và lưu vào ô nhớ mới - 1

a = 2;
//Sửa giá trị của biến a và cập nhật lại ô nhớ - 2

console.log(b) //1
```
#### Tham chiếu
```
let a = { name: "cat" }
//Tạo ra biến a, lưu giá trị của a vào ô nhớ và gán lại địa chỉ ô nhớ cho biến a (a = #a001)

let b = a
//Tạo ra biến b và gán giá trị của biến a cho b, ở đây chính là địa chỉ địa chỉ ô nhớ của a (b =#a001)

a.name = "dog"
//Sửa giá trị của biến a thì giá trị trong ô nhớ được cập nhật

console.log(b)
// { name: "dog" }
```
### BT6. Phân biệt callback, async await, Promise 
Callback: Callback là một hàm sẽ được thực hiện sau khi một hàm khác đã thực hiện xong

### BT7. Phân biệt sự khác nhau giữa  for, map, forEach
#### Khai báo For
```
for (var i; i <10 ; i++>)
{
	// Code here
}
```
#### Khai báo ForEach
```
const fruits = ["apple", "orange", "cherry"];
fruits.forEach(myFunction);
 
function myFunction(item, index) {
  text += index + ": " + item + "<br>"; 
}
```
#### Khai báo Map
```
const numbers = [4, 9, 16, 25];
console.log(numbers.map(Math.sqrt));
```

- Sử dụng map sẽ nhận được một mảng mới so với mảng ban đầu
- forEach thì không nhận già trị trả về
### BT8. Phân biệt sự khác nhau giữa some, every
#### Every
```
const numbers = [6, 7, 8, 9]
console.log(numbers.every(number => number > 5))
```
- Nếu tất cả các phần tử trong mảng thoả mãn một hoặc nhiều điều kiện. Hàm này sẽ trả về true, nhưng chỉ cần có 1 phần trử không thoả mãn điều kiện (failed), thì hàm này sẽ trả về false.
#### Some
```
const numbers = [15, 2, 3, 4, 5]
console.log(numbers.some(number => number > 10)) // true
```
- Lặp tất cả các phần tử trong một Array, chỉ phần 1 phần tử thoả mãn điều kiện thì Array này sẽ trả về true
### BT9. Phân biệt worker, child process
### BT10. Blocking, non blocking, vì sao Nodejs chạy đơn luồng mà không bị blocking.