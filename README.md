# _Creating Interactivity with CSS and JavScript_

### Using CSS to create Interactivity
![](https://uphinh.vn/images/2022/03/09/b8cf4c8e070d772a2881ac2e18febee8.png)
![](https://uphinh.vn/images/2022/03/09/4f0b7ec1c11050d3694ba66a85eb8b9f.png)
### Incorporating JavaScript
##### JavaScript Terminology
```
    documnet.write("Good Morning");
```
Event Handlers
![](https://uphinh.vn/images/2022/03/09/4b31a7690d1d15e49720f97d73569615.png)
##### Writing JavaScript Code
```
// Single line comment syntax
/* Multiple line 
comment syntax */

foodTwo = pepper;
foodOne = squash; foodTwo = pepper;

```
Or
```
<script>
 JavaScript statements;
</script>
```
Or
```
<script src="scripts/myscripts.js"></script>
```
##### DOM Methods
Example:
```
var logo = document.getElementById("ffc-logo");
```
Methods:
![](https://uphinh.vn/images/2022/03/09/a520fec7bac4e8803f9ed77fbecb7922.png)

##### Using if/else Statements
```
function day() {
 var day = document.getElementById("date");
 if (day === "Saturday") {
 document.write("I love Saturdays");
 } else {
 document.write("I wish it was Saturday");
 }
}
```