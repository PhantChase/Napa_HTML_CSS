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
### BT7. Phân biệt sự khác nhau giữa  for, map, forEach
### BT8. Phân biệt sự khác nhau giữa some, every
### BT9. Phân biệt worker, child process
### BT10. Blocking, non blocking, vì sao Nodejs chạy đơn luồng mà không bị blocking.