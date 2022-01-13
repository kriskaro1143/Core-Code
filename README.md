# Core-Code
Core Code Bootcamp
***
**Week challenges (Tuesday)**
1.	Watch video about Compilation and Interpretation: Done!
***
2.	Java language is compiled or interpreted? A.// Interpreted
***
3.	Create an algorithm to calculate the equivalent of your local currencty to USD.

dolar = 7.71
while True:
	quetzales = float(input("Cuantos quetzales desea convertir"))
	dolares = quetzales / dolar
	print ("{} quetzales equivales a {} dolares".format(quetzales, dolares))
	otra = input("¿Desea realizar otro cálculo?")
	if otra ** "n" or otra ** "N":
		break
***
4.	Read about Pseudocode: Done!
***
5.	Why is Pseudocode helpful? A.// It is helpful because it´s a proper way to find a solution for coding problems, showing step by step how to solve it using a language easily to understand for people.
***
6.	Create a pseudocode to calculate the approximated age of a user base on the year they born.

Escribir “Ingrese la fecha de nacimiento”
Leer fnac

Escribir “Ingrese la fecha actual”
Leer factual

Edad = factual -fnac

Imprimir “La edad de la persona es: “, edad, “ años”
***
7.	Read about flowcharts: Done!
***
8.	Why are flowcharts important to us as developers? They are important since allow us to show the proper solution or steps to follow in a clear visual way and handle or modify (if necessary) our process looking for the right solution.
***
9.	Search about High-level languages and Low-level languages. Done!
***
**Week challenges (Wednesday)**
1. 	Learn about binary, decimal and hexadecimal numbers. **Done!**
***
2.	Translate the year you where born **(1991)** to binary, decimal and hexadecimal

	Binary: **11111000111**
	
	Decimal: **1024 + 512 + 256 + 128 + 64 + 4 + 2 + 1 = 1991**
	
	Hexadecimal: **7C7 (7 + 12 + 7)**
***
3.	Translate 51966 into hexadecimal and binary

	Binary: **1100101011111110**
	
	Hexadecimal: **C A F E (12 + 10 + 15 + 14)**
***
4.	Use a Low-level language, for example MIPS aseembler. **Done!**

![image](https://user-images.githubusercontent.com/96300815/149368749-a3628364-a4c3-4702-a563-9a8222130290.png)

***
5. 	Base on the examples and the guide of the low-level language: 

5.1 Create a program to add two numbers given by the user 

.data
	number1: .asciiz "\nIngrese el primer numero: "
	number2: .asciiz "\nIngrese el segundo numero: "
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
		
.data
	result_message: .asciiz "\nEl resultado es: "
.text
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


