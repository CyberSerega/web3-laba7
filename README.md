<h1 align="center" paddin> МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>

<p align="center">Лабораторная работа №7. «Разработка серверных скриптов». </p>

<p align="right">Выполнил: Рогаль Сергей Александрович</p>
<p align="right">Проверил: Соболев Е. И.</p>

<p align="center">г. Южно-Сахалинск <br> 2023 год</p>

<h2 align="center">Введение</h2>
<p align="justify">PHP — язык программирования, который наиболее распространён в сфере веб-разработки.
В настоящее время PHP является одним из лидеров среди серверных языков программирования, применяющихся для создания динамических веб-сайтов и веб-приложений. Большая часть коробочных систем управления сайтами написана именно на PHP, язык поддерживается подавляющим большинством хостинг-провайдеров, Язык получил широкое распространение благодаря своей простоте, скорости, мультипарадигмальности, богатой функциональности и кроссплатформенности.
</p>

<h2 align="center">Цели и задачи</h2>
<palign="justify">Цели: решить задачи с применением языка PHP</p>
<palign="justify">Задачи: применить технологии PHP.</p>

<h2>Решение задач</h2>

```php
<h4>Задание 1: </h4>
<?php
$var = "hello";
echo $var[0];
echo $var[1];
echo $var[4];
?>


<h4>Задание 2: </h4>
<?php
$sec = 60*60;
echo "В часе $sec секунд"
?>


<h4>Задание 3: </h4>
<?php
	$var = 1;
	$var += 12;
	$var -= 14;
	$var *= 5;
	$var /= 7;
	$var += 1;
	$var -= 1;
	echo $var;
?>


<h4>Задание 4: </h4>
<?php
	$a = 3;
	echo "Значение переменной \$a равно $a";
?>


<h4>Задание 5: </h4>
<?php
	$a = 10;
	$b = 2;
	$c = $a+$b;
	echo "\$a+\$b = $c <br>";
	$c = $a-$b;
	echo "\$a-\$b = $c <br>";
	$c = $a*$b;
	echo "\$a*\$b = $c <br>";
	$c = $a/$b;
	echo "\$a/\$b = $c <br>";
?>


<h4>Задание 6: </h4>
<?php
	$a = 10;
	$b = 2;
	$c = 5;
	$result = $a+$b+$c;
	echo "\$a+\$b+\$c = $result";
?>


<h4>Задание 7: </h4>
<?php
	$a = 17;
	$b = 10;
	$c = $a-$b;
	$d = 7;
	$result = $c+$d;
	echo "\$result = $result";
?>


<h4>Задание 8: </h4>
<?php
	$a = 'Привет, Мир!';
	echo $a;
?>



<h4>Задание 9: </h4>
<?php
	$text1 = 'Привет, '; 
	$text2 = 'Мир!'; 
	echo $text1 . $text2;
?>


<h4>Задания 10,11: </h4>
<?php
	$name = 'Сергей'; 
	$age = '19'; 
	echo "Привет, $name <br>";
	echo "Мне $age лет!";
?>

<h4>Задание 12: </h4>
<?php
	$text = 'abcde';  
	echo $text[0] . $text[2] . $text[4];
?>



<h4>Задание 13: </h4>
<?php
	$text = 'abcde';  
	$text[0] = '!';
	echo "Вот измененная строка $text";
?>


<h4>Задание 14: </h4>
<?php
	$num = 12345;
	$sum = 0;
    while($num!=0)
	{
		$sum+=$num%10;
		$num = $num/10;
	}	
	echo "Сумма цифр числа 12345 равна $sum";
?>


			
<h4>Задание 15: </h4>
<?php
	echo "В часе " . 60*60 . " секунд <br>";
	echo "В сутках " . 60*60*24 . " секунд <br>";
	echo "В месяцe " . 60*60*24*30 . " секунд <br>";
?>


<h4>Задание 16: </h4>
	<?php
	$hour = 60 * 60;
	echo $hour . ' Секунд в часе! ';
	$day = $hour * 24;
	echo $day . ' Секунд в дне! ';
	$month = $day * 30;
	echo $month . ' Секунд в месяце! ';
	?>


<h4>Задание 17: </h4>
<?php
	date_default_timezone_set('Asia/Sakhalin');
	echo date('h:i:s a', time());
?>


<h4>Задание 18: </h4>
<?php
	$num = 7;
	echo "Это число $num <br>";
	$num*=$num;
	echo  "Это его квадрат: $num"
?>		


<h4>Задание 19: </h4>
<?php
$var = 47;
$var += 7;
$var -= 18;
$var *= 10;
$var /= 20;
echo $var;

?>


<h4>Задание 20: </h4>
<?php
$text = 'Я';
$text .=' хочу';
$text .=' знать';
$text .=' PHP!';
echo $text;
?>


<h4>Задание 21: </h4>
<?php
$var = 10;
$var++;
$var++;
$var--;
echo $var;
?>


<h4>Задание 22: </h4>
<?php
$var = 10;
$var +=7;
$var++;
$var--;
$var +=12;
$var *=7;
$var -=15;
echo $var;
?>

```
<p>Скрипт для генерации QR-кодов</p>

```javascript
const express = require('express');
const QRCode = require('qrcode');

const app = express();

app.get('/generate', async (req, res) => {
  const url = req.query.url;

  if (!url) {
    return res.status(400).send('URL не указан.');
  }

  try {
    const qr = await QRCode.toDataURL(url);
    res.send(`<img src="${qr}" />`);
  } catch (err) {
    res.status(500).send('Ошибка при создании QR-кода.');
  }
});
app.get('/', async (req, res) => {
    res.send("Создание QR-кода. Пример:/generate?url=https://htmlacademy.ru")
  });

app.listen(3000, () => {
  console.log(`Сервер запущен на порту 3000`);
});
```
<p>Скрипт отправки Email</p>

```javascript
const nodemailer = require('nodemailer');

let transporter = nodemailer.createTransport({
    host: '',
    port: ,
    secure: false,
    auth: {
        user:"user",
        pass: "pass",
    },
});

let result = transporter.sendMail({
    from: 'me',
    to: 'you',
    subject: 'Hello from bot',
    text: 'Hello from bot'
});
console.log(result);
```

<p>Скрипт отправки Email</p>
<p>parser.js</p>

```javascript
const axios = require("axios");
const getData = async() => {
try{
    const response = await axios.get("https://books.toscrape.com/"); 
    let res = response.data.match(/<p class=\"price_color\">(.*)<\/p>/g);    
    let res1 = response.data.match(/<a href=\"catalogue(.*)title(.*)<\/a>(.*)/g); 
    res = res.map(item => item.split('>')[1].slice(1, -3));
    res1 = res1.map(item => item.match(/title=\"(.*)\"/)[1]);
    //console.log(res, res1);
    const books = [];
    for(let i=0; i<res.length; i++){
        books.push([res[i], res1[i]]);
    } 
    return books;
}
catch(e)
{
    console.log(e);
}
}
module.exports.books = getData;
```

<p>database.js</p>

```javascript
const getData = require('./parser.js');
const mysql = require('mysql');

//Данные нашей базы данных
const dbConfig = {
host: 'host'
user: 'user',
password: 'password',
database: 'database'
};

//подключение к базе данных
function createDbConnection() {
return mysql.createConnection(dbConfig);
}

//SQL-запрос
function executeQuery(connection, query) {
connection.query(query, (error, results) => {
if (error) {
console.error('Ошибка выполнения SQL-запроса:', error);
}
});
}
//парсинг данных 
async function parseToDb() {
try {  
  const connection = createDbConnection();
  let books  = getData.books();
  books.then(result=>{
    for(let i=0; i<result.length; i++){
      const query = `INSERT INTO \`table\` (title, price) VALUES ('${result[i][1]}', ${result[i][0]})`; 
      console.log(query);       
      executeQuery(connection, query);
    }  
  });
} catch (error) {
console.error('Ошибка при запросе', error.message);
}
}
parseToDb();
```

<p>Codewars</p>
<p>Breaking Chocolate Problem</p>

```javascript
function breakChocolate(n,m) {
  if(n*m-1<0) return 0;
  return n*m-1;
}
```

<p>Playing with digits</p>

```javascript
function digPow(n, p){
  var resNum = 0;
  var temp = n.toString();
  for(let i=0; i<temp.length; i++){
    resNum+=Math.pow(Number(temp[i]),p);
    p++;
  }
  if(resNum%n==0) return resNum/n;
  else return -1;
}
```
<p>The reject() function</p>

```javascript
function reject(array, predicate) {
  let newArr = [];
  for(let i = 0; i<array.length; i++){
    if (!predicate(array[i])) newArr.push(array[i]);
  }
  return newArr;
}
```

<p>Deodorant Evaporator</p>

```javascript
function evaporator(content, evap_per_day, threshold){ 
  var days = 0;
  var hold = content*threshold/100;
  while(content>=hold){
    content -= content*evap_per_day/100;
    days++;
  }
  return days;
}
```

<p>Fibonacci's FizzBuzz</p>

```javascript
var fibsFizzBuzz = function(n) {
    function FibNum(num){
      if(num<=2) return 1;
      let first = 1;
      let second = 1;
      let sum=0;
      for(let i = 3; i<=num; i++){
        sum = first+second;
        first = second;
        second = sum;
      }
      return sum;
    }
  var res = [];
  for(let i=1; i<=n; i++){
    var num = FibNum(i);
    if(num%3==0){
      if(num%5==0) res.push('FizzBuzz');
      else res.push('Fizz');
    }
    else if(num%5==0) res.push('Buzz');
    else res.push(num);
  }
  return res;
}
```

<p>Replace With Alphabet Position</p>

```javascript
function alphabetPosition(text) {
  var res = "";
  text = text.toLowerCase();
  for(let i = 0; i<text.length; i++){
    if (text[i].match(/[a-z]/i)) res += (text[i].charCodeAt()-'a'.charCodeAt()+1).toString()+" ";
  }
  res = res.trimEnd();
  return res;
}
```

<p>Equal Sides Of An Array</p>

```javascript
function findEvenIndex(arr)
{
  let leftSum = 0;
  let rightSum = arr.reduce((acc, item) => acc+item, 0);
  for(let i = 0; i<arr.length; i++){
    rightSum-=arr[i];
    if (leftSum==rightSum) return i;
    leftSum+=arr[i];    
  }
  return -1;
}
```

<p>Calculate average</p>

```javascript
function findAverage(array) {
  let sum = 0;
  for(let i = 0; i<array.length; i++){
    sum+=array[i];
  }
  return array.length==0 ? 0 : sum/array.length;
}
```

<p>Scrolling Text</p>

```javascript
function scrollingText(text){
  text = text.toUpperCase();
  const res = [text];
  for(let i = 0; i < text.length-1; i++){
    let firstSymb = text[0];
    text = text.slice(1);
    text+=firstSymb;
    res.push(text);
  }
  return res;
}
```

<p>Bumps in the Road</p>

```javascript
let bump = (x) => x.split('n').length-1>15 ? "Car Dead" : "Woohoo!";
```

<p>Coding Meetup #1 - Higher-Order Functions Series - Count the number of JavaScript developers coming from Europe</p>

```javascript
function countDevelopers(list) {
  let count = 0;
  for(let i = 0; i < list.length; i++){
    if(list[i].continent === "Europe" && list[i].language ==="JavaScript") count++;
  }
  return count;
}
```


<h2 align="center">Вывод</h2>
<p align="justify">Таким образом, я освежил в памяти работу с PHP, поработал с базой данных, написал скрипт для парсинга сайта, скрипт для отправки электронной почты, с помощью Node JS создал сервер для генерации QR-кодов, все поставленные цели были выполнены. </p>
