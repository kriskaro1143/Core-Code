# Core-Code
Core Code Bootcamp
***
**Week challenges (Tuesday 11)**
1. Watch video about Compilation and Interpretation: Done!
***
2. Java language is compiled or interpreted? A.// Interpreted
***
3. Create an algorithm to calculate the equivalent of your local currencty to USD.

dolar = 7.71
while True:
	quetzales = float(input("Cuantos quetzales desea convertir"))
	dolares = quetzales / dolar
	print ("{} quetzales equivales a {} dolares".format(quetzales, dolares))
	otra = input("¿Desea realizar otro cálculo?")
	if otra ** "n" or otra ** "N":
		break
***
4. Read about Pseudocode: Done!
***
5. Why is Pseudocode helpful? A.// It is helpful because it´s a proper way to find a solution for coding problems, showing step by step how to solve it using a language easily to understand for people.
***
6. Create a pseudocode to calculate the approximated age of a user base on the year they born.

Escribir “Ingrese la fecha de nacimiento”
Leer fnac

Escribir “Ingrese la fecha actual”
Leer factual

Edad = factual -fnac

Imprimir “La edad de la persona es: “, edad, “ años”
***
7. Read about flowcharts: Done!
***
8. Why are flowcharts important to us as developers? They are important since allow us to show the proper solution or steps to follow in a clear visual way and handle or modify (if necessary) our process looking for the right solution.
***
9. Search about High-level languages and Low-level languages. Done!
***
**Week challenges (Wednesday 12)**
1.  Learn about binary, decimal and hexadecimal numbers. **Done!**
***
2. Translate the year you where born **(1991)** to binary, decimal and hexadecimal

	Binary: **11111000111**
	
	Decimal: **1024 + 512 + 256 + 128 + 64 + 4 + 2 + 1 = 1991**
	
	Hexadecimal: **7C7 (7 + 12 + 7)**
***
3. Translate 51966 into hexadecimal and binary

	Binary: **1100101011111110**
	
	Hexadecimal: **C A F E (12 + 10 + 15 + 14)**
***
4. Use a Low-level language, for example MIPS aseembler. **Done!**

![image](https://user-images.githubusercontent.com/96300815/149368749-a3628364-a4c3-4702-a563-9a8222130290.png)

***
5.  Base on the examples and the guide of the low-level language: 

	5.1 Create a program to add two numbers given by the user 

.data

	number1: .asciiz "\nIngrese el primer numero: "
	
	number2: .asciiz "\nIngrese el segundo numero: "
	
	result_message: .asciiz "\nEl resultado es: "
	
.text

	main:
	
		li $v0, 4
		la $a0, number1
		syscall

		li $v0, 5
		syscall

		move $t0, $v0
	
		li $v0, 4
		la $a0, number2
		syscall

		li $v0, 5
		syscall

		move $t1, $v0
		
		
		add $t2, $t0, $t1

		li $v0, 4
		la $a0 result_message
		syscall

		li $v0, 1
		move $a0, $t2
		syscall
		
![image](https://user-images.githubusercontent.com/96300815/149371909-e67ac4a2-ce5b-4bba-857d-546211968f1f.png)

![image](https://user-images.githubusercontent.com/96300815/149371967-dd2f5dc6-ea47-4941-ae62-9bbeaa1a902f.png)

	5.2 Create a program that display your name

.data

	mensaje: .asciiz "Cristian Fuentes\n"	
	
.text

	li $v0, 4
	
	la $a0, mensaje
	
	syscall
	
![image](https://user-images.githubusercontent.com/96300815/149392348-5b8dca42-5a4f-4ca9-96c9-d91538714f70.png)

***
#**Week challenges (Thursday 13)**

1. Search for real word applications of Javascript **Done!**

2. (optional but great) Watch this video **Done!**

3. (optional but great) Watch this video **Done!**

4. Follow the github course. **Done!**

***

#2nd Week challenges 

**(Monday 17)**

1. Follow the github course

2. Watch this video about **What Are Data Types?  Done!**

3. Read about "Basic math in JavaScript — numbers and operators" **Done!**

4. Create an account in Codewars **Done!** 

***
**(Tuesday 18)**

1. Multiply

function multiply(a, b){

  return a * b
  
}

2. ASCCI Total

function uniTotal (c) 

{

    var sum=0;
    
    for (var i=0; i<c.length; ++i)
    
        sum+=c[i].charCodeAt();
	
    return sum;
    
}

3. Get character from ASCII Value

function getChar(c) {

    return String.fromCharCode(c)
}

4. Binary Addition

function addBinary(a,b){

  return (a+b).toString(2)
  
}

5.  Student's Final Grade

function finalGrade (exam, projects) {

  if(exam > 90 || projects > 10) return 100;
  
  if(exam > 75 & projects >= 5) return 90;
  
  
  if(exam > 50 & projects >= 2) return 75;
  
  return 0;
  
}
***
**(Wednesday 19)**

1.  Holiday Viii-Duty Free

function dutyFree(normPrice, discount, hol){

  return(Math.floor(hol / normPrice / discount * 100))
  
}


2.  Twice as Old

function twiceAsOld(dadYearsOld, sonYearsOld) {

  // your code here
  
  return Math.abs(dadYearsOld - (sonYearsOld*2));
  
}


3.  Valid Spacing

function validSpacing(s) {

  // write your code here
  
  if(s.length==0)
  
    return true;
    
  var arr=s.split(' ');
  
  for (var i=0; i<arr.length; i++)
  
    if (arr[i].length==0)
    
      return false;
      
  return true;
  
}


4.  Fake Binary

function fakeBin(x){

  return x.split('').map(a => a < '5' ? "0" : "1").join("");
  
}

***
**(Thursday 20)**

1.  Exclamation marks series #2: Remove all exclamation marks from the end of sentence

function remove (string) {  

  return string.replace(/!+$/, '');
  
}


2.  Vowel remover

function shortcut (string) {

  return string.replace(/[aeiou]/gi, '');
  
}


3.  Rock Paper Scissors!

const rps = (p1, p2) => {

  if (p1 === p2) return "Draw!";
  
  var rules = {rock: "scissors", paper: "rock", scissors: "paper"};
  
  if (p2 === rules[p1]) {
  
    return "Player 1 won!";
    
  }
  
  else {
  
    return "Player 2 won!";
    
  }
  
};


4.  Persistent Bugger


function persistence(num) {

   //code me
   
  if (num.toString().length === 1) {
  
    return 0;
    
  }
  
  var mult = 1;
  
  var splitStr = num.toString().split("");
  
  for (var i = 0; i < splitStr.length; i++) {
  
    mult *= parseFloat(splitStr[i]);
    
  }
  
  return 1 + persistence(parseFloat(mult));
  
}



#5.   1st Core Challenge

***I´m Cristian, a talent adquisition specialist currently learning about programming (JavaScript, React & Node.js). I would like to convert myself in a really good developer and offer practical solutions to the ITS industry. I´m a self-taught-person, compromise and always looking for new challenges that dare my skills!***

***

**(Monday 24)**

1. Who likes it?

function likes(names) {

  // TODO
  
var templates = [

    'no one likes this',
    
    '{name} likes this',
    
    '{name} and {name} like this',
    
    '{name}, {name} and {name} like this',
    
    '{name}, {name} and {n} others like this'
    
  ];
  
  var idx = Math.min(names.length, 4);
  
  
  return templates[idx].replace(/{name}|{n}/g, function (val) {
  
    return val === '{name}' ? names.shift() : names.length;
    
  });
  
}







2.Bit Counting


var countBits = function(n) {

   // make an array with the bit result
   
   const base = (n).toString(2).split('');
   
   
   // make a sum with the array and make the index a Number
   
   const result = base.reduce((sum, num) => sum + Number(num), 0);
   
   
   return result;
   
}







3. Decode the Morse code


decodeMorse = function(morseCode){

    //your code here
    
  return morseCode
  
    .trim()
    
    .split(/  | /)
    
    .map( (code) => MORSE_CODE[code] || ' ')
    
    .join('');
    
}


***


**(Tuesday 25)**

1. Your order, please


function order(words){
  
  return words.split(' ').sort(function(a, b){
  
      return a.match(/\d/) - b.match(/\d/);
      
   }).join(' ');
   
}   





2. Counting Duplicates


function duplicateCount(text){

  return (text.toLowerCase().split('').sort().join('').match(/([^])\1+/g) || []).length;
  
}






3. Simple Pig Latin


function pigIt(str){

  //Code here
  
  str = str.trim().split(/\s{1,}/);
  
    return str.map(val => {
    
        if (/^[A-Za-z]+$/.test(val)) {
	
            return `${val.slice(1)}${val.slice(0, 1)}ay`;
	    
        }
	
        return val;
	
    }).join(' ');
    
}


***

**(Wednesday 26)**


1. Valid Parentheses


function validParentheses(parens){

  var n = 0;
  
  for (var i = 0; i < parens.length; i++) {
  
    if (parens[i] == '(') n++;
    
    if (parens[i] == ')') n--;
    
    if (n < 0) return false;
    
  }
  
  
  return n == 0;
  
}





2. Convert string to camel case


function toCamelCase(str){

  var regExp=/[-_]\w/ig;
  
  return str.replace(regExp,function(match){
  
        return match.charAt(1).toUpperCase();
	
   });
   
}






3. Unique In Order


var uniqueInOrder=function(iterable){

  return [...iterable].filter((a, i) => a !== iterable[i-1])
  
}


***

**(Thursday 27)**


1. Fold an array



function foldArray(array, runs) {

  if (!runs) return array;

  var result = [];
  
  // new Array
  
  for (var i = 0; i < Math.ceil(array.length / 2); i++) {
  
    result[i] = array.length -i - 1 === i ? array[i] : array[i] + array[array.length - i - 1];
    
  }
  
  
  return foldArray(result, runs - 1);
  
}





2. Encrypt this!


var encryptThis = function(text) {

  return text.replace(/(\w)(\w?)((\w*)(\w))?/g, 
  
  (word, first, second, tail, middle, last) => [first.charCodeAt(0), last, middle, second].join(''));
  
}





3. Format a string of names like 'Bart, Lisa & Maggie'.(retired)


function list(names){

  if (names.length > 1) {
  
    return `${otherNames(names)} & ${names[names.length - 1].name}`
    
  } else if (names.length === 1) {
  
    return names[0].name
    
  }
  
   return '';
   
 }
 
 
 function otherNames(array) {
 
   return array.splice(0, array.length - 1).map(person => person.name).join(', ');
   
 }

***
