		---- caracteristicas do C++(C Plus Plus) ----

	<case sensitive>
		* diferencia entre uppercase e lowercase
		
	<linguagem compilada>
		* usa um compilador
		
	<multi-paradigma>
		* possui suporte a linguagem imperativa(ou procedural), oop(object oriented Programming) e generica

	<general purpuse>
		* pode ser usado para multiplos propositos
	
	<estaticamente tipada>
		* seus data-type nao podem ser mudados e devem ser declarados no inicio do arquivo
		
	
[exemplo de arquivo c++]
		#include <iostream>
		int main() {
		std::cout << "hello world" << std::endl;
		return 0;
		}
		
[comentarios]
		> no c++ usa-se '//' e '/**/' para comentarios
			* '//' usado para comentar uma unica linha
			* '/**/' usado para comentar multiplas linhas
		
[fundamental data types]
	> int 
		* integer, numeros inteiros, 2 ou 4 Bytes
		* pode conter dados de -2147483648 ate 2147483647
		* int salary = 57000;
		
	> float
		* floating point, numeros reais, 4 Bytes
		* pode conter dados decimais e exponenciais
		* float area = 64.74;
		
	> double
		* double float point, numeros com ponto(numeros reais), 8 Bytes
		* contem duas vezes a precissao de float
		* double volume = 134.54342;
		
	> char 
		* character, letras unicas(a, b, c, etc), 1 Byte
		* contem characters, usa-se entre single quotes(')
		* char gpa = 'F';
		
	> string
		* strings, palavras ou frases completas, 
		* contem uma sequencia de caracteres(testo)
		* nao built-in
		* usa-se entre double quotes(")
		* string name = "jhon santos";
		
	> bool
		* boolean, true ou false, 1 byte
		* contem os valores true e false
		* bool condition = false;

	> void
		* empty, 0 Byte
			
[type modifiers]
	> pode-se modificar os types fundamentais(int, double e char) usando 4 modifiers(signed, unsigned, short e long)
	> int
		> signed int
			* 4 Bytes
			* mesmo que int
			
		> unsigned int
			* 4 Bytes
			* apenas numeros positivos
			
		> short 
			* 2 Bytes
			* usado para integers pequenos(de -32768 a 32767)
			
		> unsigned short
			* 2 Bytes
			* usado para integers pequenos e possitivos(de 0 a 65535)
			
		> long 
			* ate 4 Bytes
			* usado para integers largos(mesmo que long int)
			
		> unsigned long
			* 4 Bytes
			* usado para integers largos e possitivos ou 0(mesmo que unsigned long int)
			
		> long long
			* 8 Bytes
			* usado para integers muito largos(mesmo que long long int)
			
		> unsigned long long 
			* 8 Bytes 
			* usado para integers muito largos e positivos ou 0(equivalente a unsigned long long int)
			
	> double
		> long double
			* 12 Bytes
			* usado para largos floating-point numeros
	> char
		> signed char
			* 1 Byte
			* usado para characters (de -127 a 127)
			
		> unsigned char
			* 1 Byte 
			* usado para characters(de 0 para 255)
				
[Variables]
	> para definir uma variavel define-se primeiro o data type e entao o nome
		* int age;
		
	> pode-se tambe alocar um valor da definicao diretamente
		* int age = 19;
		
	> regras para nomiar uma variavel:
		* unicamente alphabetos, numeros e underscore(_)
		* nao pode iniciar com um numero
		* e preferivel iniciar a variavel com lowercase
		* nao pode ser uma 'keyword', como: int, class, for, etc...
		* pode-se inciar com underscore mas nao e aconselhado
		* aconselhado usar nomes coerentes, exemplo: first_name
		* nao pode conter espacos(' ')
		* camelCase
			# uppercase para separar palavras
		* snake_case
			# underscore para separa palavras
			
	> literals
		> integers
			* decimal (base 10)
				# 0, -9, 22, etc...
				
			* octal (base 8)
				# 021, 077, 033, etc...
				# sempre inicia com '0'
				
			* hexadecimal (base 16)
				# 0x7f, 0x2a, 0x521, etc...
				# sempre inicia com '0x'
				
		> floating point
			* fractional
				# -2.0
				# 0.0000231
				
			* exponent
				# -0.22E-5
					> E-5 equivale a 10^-5
					
		> escape sequences
			* usado quando e nescessario usar characters que nao podem ser typed ou possui um uso especial em c++
			* usa-se backslash(\) para ignorar o proximo character
			* \b
				# backspace
			* \f
				# form feed
			* \n 
				# newline
			* \r 
				# return
			* \t 
				# horizontal tab
			* \v 
				# vertical tab
			* \\
				# backslash
			* \'
				# single quotation mark
			* \"
				# double quotation mark
			* \?
				# question mark
			* \0
				# null character
			
		> string
			> string literal sao sequencias de characters dentro de double quotation mark
			> "good"
				> uma string normal
				
			> ""
				> uma string vazia(null)
				
			> "    "
				> uma string com espacos dentro
				
			> "x"
				> uma string com um unico caracter dentro
			
			> "hello\n"
				> uma string com um newline
				
		> contants
			> constant sao variaveis cujo valor nao pode ser mudados
			> const int pi = 3.1415
			> o valor nao pode ser mudado portanto se for tentado
				> pi = 32; //ira dar erro pois pi e uma contant
				
	> Storage Class
		> all variables has data type and storage class 
		> for exemple the data type: int, float, char, etc...
		> and the storage class are: local variable, global variable, static local variable, register variable, thread local storage
		
		> Local variable
			> is a Variable defined inside a function that is called local or automatic variable
			> its scope is only limited to the function where is defined
			
		> global variable
			> is a variable defined outside all functions 
			> its scope is the whole program and can be accessed at any part of the program
			
		> static local variable
			> is a variable similar to local variable but start at the calling of the function and only end at the end of the program
			> to use that variable use the keyword: static
			> ex.: static int age;
			
		> register variable 
			> is used for specifying registers
			> is deprecated so not recomended
			
		> thread local storage
			> is a mechanism by which variables are allocated such that there is one instance of the variable lper thread
			> is used the keyword thread_local
				
[output e input]
	> no c++ usa-se 'std::cout <<' para dar output em um dado
		> ex.: 
			> std::cout << "hello" << std::endl;
				> ira mostrar na tela: hello
				> 'std' significa 'stardard', e a biblioteca padrao onde reside o 'cout'
				> pode-se tambe adicionar 'using std::cout' ao header para eliminar o 'std::' do codigo
				> 'std::endl' tem o mesmo papel de '\n' ou seja inserir uma newline
				> toda linha em c++ termina com ';' para demostrar que a linha termina ali
				
	> usa-se 'std::cin >> ' para dar input em um dado do usuario
		> ex.:
			> int age;
			> std::cin >> age;
				> ira enviar o input do usuario para a variavel age
				
		> o 'std::cin' apenas guarda palavras(antes de um espaco) para guardar frases completas(com espacos) precisamos usar uma funcao como: getline()
			> string name;
			> getline(cin, name)
				> ira guardar toda a string dentro da variavel 'name'
					
[operators]
	> arithmetic operators
		> '+' addition
		> '-' subtraction
		> '*' multiplication
		> '/' division
		> '%' modulo(resto da divisao)
		
	> increment e decrement operators
		> '++' increase by 1
			num = 1;
			num++ == 2;
			> mesmo que num = num + 1;
		> '--' decrease by 1
			num = 1;
			num-- == 0;
			> mesmo que num = num - 1;
			
	> assignment operators
		> '=' assign, ex.: a = b;
		> '+=', equal to a = a + b;
		> '-=', equal to a = a - b;
		> '*=', equal to a = a * b;
		> '/=', equal to a = a / b;
		> '%=', equal to a = a % b;
		
	> relational operators
		> '==' is equal to
		> '!=' not equal to
		> '>' greater than
		> '<' less than
		> '>=' greater or equal to
		> '<=' less or equal to
		
	> logical operators
		> '&&', logical 'AND'
			> operand1 && operand2
			> true if all operand are true
			
		> '||', logical 'OR'
			> operand1 || operand2
			> true if at least one of the operand are true
			
		> '!', logical 'NOT'
			> !operand
			> true only if the operand are false
			
	> Bitwise operators
		> usado para fazer operacoes com bits individuais, apenas pode ser usado com data type do tipo 'char' e 'int'
		> '&' binary 'AND'
		> '|' binary 'OR'
		> '^' binary 'XOR'
		> '~' binary One's Complement
		> '<<' binary shift left
		> '>>' binary shift right
		
	> Others operators
		> 'sizeof'
			> retorna o tamanho em bytes de um data type
			> sizeof(int); 
				> 4
			
		> '?:'
			> retorna o valor baseado na condicao
			> string result = (5 > 0) ? "yes" : "nop"; 
				> "yes"
				
		> '&'
			> representa o memory address de um operando
			> &num;
				> memory address de num
		
		> '.'
			> acessa membros strutura variavel ou class ou objects
			> s1.marks = 92;
				> acessa o atributo 'marks' dentro do objeto 's1' e altera o valor para '92'
				
		> '->'
			> usado com pointers para acessar variaveis da class
			> ptr -> marks = 92;
				> mesmo que ptr.mark = 92; 
					> utilizado quando '.' nao pode ser usado
			
		> '<<'
			> print o valor de output
			> cout << 5;
				> 5
				
		> '>>'
			> pega o valor de input do usuario
			> cin >> num;
				
[flow control]
	> if...else statement
		> if (condition) {
			body of if statement
			
		} else if (condition) {
			body of else if statement
			
		} else {
			body of else statement
		
		}
		
	> nested if...else statement
		> if (condition) {
			if (condition) {
				body of if statement
				
			} else {
				body of else statement
			
			}
		}
		
	> switch...case statement
		> switch (expression) {
			case constant1:
				//code to be executed if expression is equal to constant1
				break;
				
			case constant2:
				//code to be executed if expression is equal to constant2
				break;
				
			case constant3:
				//code to be executed if expression is equal to constant3
				break;
				
			case constant4:
				//code to be executed if expression is equal to constant4
				break;
				
			default:
				//code to be executed if expression doesn't match any constant
				break;
				
		}
		
	> for loop
		> for (initialization; condition; update) {
			//body of loop
			
		}
		
		> ex.:
			> for(int count = 0; count <= 5; count++) {
				std::cout << count << std::endl;
			
			}
			
		> ranged based for loop, pode ser usado para passar por todos os conponentes de um array. ex.:
			> int num_array[] = {1, 2, 3, 4, 5};
			> for (int num : num_array) {
				std::cout << num << " ";
			
			}
			
	> while loop
		> while(condition) {
			// body of the loop
		
		}
		
		> ex.:
			> int count = 0;
			> while (count <= 10) {
				std::cout << count << " ";
				count++;
			
			}
			
		> infinite loop
			while(true) {
				//body of loop
				
			}
			
	> do...while loop
		> do {
			// body of loop
			
		} while (condition);
		
		> ex.:
			> int c = 0;
			> do {
				std::cout << c << " ";
				c++;
				
			} while(c <= 9);
				
		> infinite loop
			> int c = 1;
			> do {
				std::cout << c << " ";
				
			} while(c == 1);
			
	> break...continue
		> break pode ser usado em um statement para quebrar o loop
		> continue pode ser usado para ignorar um block de codigo para ser preechido depois
		> while(true) {
			if(condition) {
				continue; //este bloco sera ignorado, mas nao quebrara o programa
			
			} else {
				break; // encerra o loop
				
			}
		}
		
[Function]
	> funcoes sem parametros
		> returnType functionName() {
			// function body
		
		}
		
		> uma funcao pode ou nao ter parametros e deve ser declarada primeiro
		> declaring the function
			> void greet() { 
				std::cout << "hello there" << std::endl;
			
			}
			> por ser do data type void a funcao nao precissa retornar nada
			
		> uma vez declara pode-ser chamada(call) quantas vezes for nescessario
			> #include <iostream>
			> int main() {
				//calling the function
				great(); 
			
				return 0;	
			}
		
	> funcoes com parametros
		> returnType functionName(parameter1, parameter2, ...) {
			//function body
			
		}
		
		> declaring the function
			> void displayNumber(int number1, double number2, string name) {
				std::cout << "number int is " << number1 << std::endl;
				std::cout << "number double is " << number2 << std::endl;
				std::cout << "name string is " << name << std::endl;
			
			}
			
		> calling the function
			> #include <iostream>
			> int main() {
				int n1 = 20;
				double n2 = 2.21;
				string s = "john";
			
				displayNumber(n1, n2, s);
					
					
				return 0;
			}
			
	> return statement
		> retorna o valor da funcao de acordo com ser data typed
		> declaring the function
			> int addition(int a, int b) {
				int result = a + b;
				return result;
			
			}
			
		> declaring the function
			> #include <iostream>
			> int main() {
				std::cout << addition(10, 22);
			
				return 0;
			}
			
	> function prototype
		> to using a function before declaration is nescessary declary a prototype before the call
		> function prototype
			> void addition(int, int);
			
		> calling the function before declaration
			> int main() {
				addition(5, 3);
				return 0;
			}
			
		> function definition
			> void addition(int a, int b) {
				cout << (a + b);
			
			}
			
	> overloaded function
		> multiple functions with the same name is possible but, the parameter must be different
			> int test() {}
			> int test(int a) {}
			> int test(int a, double b) {}
			> double test(double a) {}
			
	> default argument
		> the dafault argument will be used if no argument is passed when the function is called
		> once is bein used a default argument all subsequent argument has to also have a default value
		> ex.:
			> void showNumbers(int num1 = 10, double num2 = 2.1) {
				std::cout << number1 << std::endl;
				std::cout << number2 << std::endl;
				
			> int main() {
				showNumbers(); //no argument is passed so will be output: number1 == 10 and number2 == 2.1
				return 0;
			}
			
	> recursive function
		> recursive function are function that call itself
		> to prevent infinite recursioin, if...else statement can be used
		> ex.:
			> int factorial(int n) {
				if (n > 1) {
					return n * factorial(n - 1);
				
				} else {
					return 1;
				
				}
			}
				
			> int main() {
				int n = 4;
				
				std::cout << "factorial of " << n << " = " << factorial(n);
				return 0;
			
			}
			
[Arrays]
	> arrays are variables that can store multiple values of the same type.
	> arrays indices start at 0, array[0] is the first element
	> the size of each element is 4, because size of 'int' is 4 bytes. meaning an array with 4 element has a size of 16 bytes.
	
	> array declaration:
		> dataType arrayName[arraySize];
			> ex.: int names[6];
				> int == data type to be stored
				> names == name of array
				> 6 == size of the array
				
	> access element in array
		> array[index];
			> ex.: names[0];
				> acess the index '0' of array
				
	> array initialization
		> initialization during declaration.
			> int ages[6] = {19, 10, 8, 17, 9, 15};
				> the array hold 6 elements
			
		> if the limite is not declared the limit isn't present.
			> int ages[] = {19, 10, 8, 17, 9, 15}
			
	> insert element in an array
		> int mark[5] = {1, 2, 3}
		
		> mark[3] = 9;
			> store value at 4th possition
			
		> mark[0] = 0;
			> change the value of teh 1st possition
			
		> std::cin >> mark[i-1];
			> take input from user and insert at last possition, in this case the 5th possition or index 4j
			> same as: std::cin >> mark[4];
			
	> display elements of an array
		> one can use a for loop to show all elements in an array
		>ex.:
			> for (int index = 0; index < 5; ++index) {
				std::cout << ages[index] << " ";
			
			}
			
	> multidimensional arrays
		> declaration
			> dataType arrayName[size][size];
				> int x[3][4];
				
		> array table
			>	   | column1 | column2  | column3 | column4
			> row1 | x[0][0] | x[0][1]  | x[0][2] | x[0][3]
			> row2 | x[1][0] | x[1][1]  | x[1][2] | x[1][3]
			> row3 | x[2][0] | x[2][1]  | x[2][2] | x[2][3]
			
		> the three-dimensional array works in an similar way.
		> float x[2][4][3] to find out the total element that a array can hold is just multiplying the elements of the array
		> 2 * 4 * 3 = 24 elements
		
		> initialization two-dimensional array
			> int test[2][3] = {{2, 4, 6}, {5, 0, 9}};
				> this array has 2 rows(test[2]) and 3 columns(test[3])
				
		> initialization three-dimensional array
			> int test[2][3][4] = {
								{{1, 2, 3, 4},{1, 0, 0, 1},{0, 9, 8, 1}},
								{{4, 3, 2, 1},{0, 1, 1, 0},{1, 8, 9, 0}}
								}
				> this array has 2 rows(test[2]) three columns(test[3]) and 3 element inside each one
				
		> display multidimentional arrays
			> for (int index1 = 0; index1 < 2; ++index1) {
				for (int index2 = 0; index2 < 3; ++index2) {
					std::cout << "x[" << index1 << "][" << index2 << "]: " << x[index1][index2] << std::endl;
				}
			
			}
			
		> passing arrays as function parameters
			> dataType functionName(arrayDatatype arrayName[arraySize]) {}
			> void display(int marks[5]) {
				for (int i = 0; i < 5; ++i) {
					std::cout << marks[i] << std::endl;
				}
			}
			
			> int main() {
				int marks[5] = {11, 22, 33, 44, 55};
				
				display(marks);
				return 0;
			}
			
[structures]
	> similar to classes is used to organaze all data of a sama type in only one place work as blueprint
	> data inside a struct is called atribute
	
	> declaration
		> struct structName {
			//atributes
			
		};
		
	> access
		> structName.atributeName;
		> structName.atributeName = "john";
		
	> ex.:
		> struct Person {
			char name[50];
			int age;
			double salary;
			
		};
		
		> int main(){
			Person p1;
			
			p1.name = "john santos";
			p1.age = 19;
			p1.salary = 1021.99;
			
			std::cout << "name: " << p1.name << std::endl;
			std::cout << "age: " << p1.age << std::endl;
			std:: << "salary: " << p1.salary << std::endl;
			
			return 0;
		}
		
	> Function and structures
		> struct Person {
			char name[50];
			int age;
			
		};
		
		> void displayData(Person); //function declaration
		
		> int main() {
			Person bill;
			
			bill.name = "Bill Chinton";
			bill.age = 55;
			
			displayData(bill);
			
			return 0;
		}
		
		> void displayData(Person bill) {
			std::cout << "\nDisplaying Information." << std::endl;
			std::cout << "Name: " << bill.name << std::endl;
			std::cout << "age: " << bill.age << std::endl;
			
		}
		
[object and class]
	> a class is a blueprint for the object
	
	> definition
		> class className {
			//Data
			//Functions
		};
		
	> ex.:
		> class Room {
			public:
				double length;
				double breadth;
				double height;
				
				double calculeArea(){
					return length * breadth;
					
				}
				
				double calculeVolume() {
					return length * breadth * height;
					
				}
		};
		
	> when a class is defined, only the specification for the object is defined, no memory or storage is allocated.
	> is a blueprint, to use the data and access the functions, a object has to be created.
	
	> syntax to define a object
		> className ObjectVariableName;
		
	> ex.:
		> Room kicken, restRoom;
		
	> to access and manipulate the data and function utilize '.'(dot)
		> className.functionName();
		> className.dataName;
		> className.DataName = 20;
		
	> ex.:
		> restRoom.length = 5.5;
		> kicken.calculeArea();
		
	> Constructors
	> are a special type of function that is automaticlly called when an object is created
	> class Wall {
		public:
			//create a constructor
			Wall() {
				//code
			}
	
	};
	
	> ex.:
		> class Wall {
			private:
				double length;
				
			public:
				Wall() {
					length = 6.6;
					std::cout << "creating a wall." << std::endl;
					std::cout << "Length: " << length << std::endl;
					
				}
		};
		
[Pointers]
	> pointers are variables that stores memory address of other variables
	> is used '&' to do that
	> ex.:
		> int var = 3;
		> std::cout << &var;
			> this will show the memory address of 'var', using hexadecimal values like: 0x7fff5f
			
	> to declare a pointers uses '*':
		> int *pointerVariable; //can be declared like this
		> int* pointerVariable; //this is the preferred syntax
		> int* pointerVariable, p;  //declaring a pointer 'pointerVariable' and a normal int variable 'p'
		
	> to assing address to pointers variables
		> int* pointVar, var;
		> var = 5
		> pointVar = &var;
		
	> to access the pointer
		> std::cout << pointVar; //this wil show the memory address of var;
		> std::cout << *pointVar; //this will show the value stored in var(5)
		
	> to add address of an array
		> int *ptr;
		> int array[5];
		
		> ptr = &array[0]; //this will save the first cell of an array
		> ptr = array; //will save only the first cell of an array
		
	> using pointer and address in functions
		> with address
		> passing the address as parameter, exclude the necessite for return a value
			> void swap(int &n1, int &n2) {
				int temp;
				temp = n1;
				n1 = n2;
				n2 = temp;
			}
			
			> swap(a, b); //calling the fuction
			
		> with pointer
			> void swap(int* n1, int* n2) {
				int temp;
				temp = *n1;
				*n1 = *n2;
				*n2 = temp;
			}
			
			> swap(&a, &b); //calling the function
			
[Memory management]
	> in c++ is possible to allocate and unalocate memory using the operators 'new' and 'delete'
	> the sytax is: pointerVariable = new dataType
		> int* pointVar;
		> pointVar = new int;
		> *pointVar = 45;
			> dynamically allocating memory for an int variable, is necessary to use a pointer to allocate memory dynamically
			> the new operator returns the address of the memory location
			
	> to return the memory to OS is used the delete operator, that is known as memory deallocation
		> the sytax is : delete pointerVariable;
		> delete pointVar;
		
[inheritance]
	> it allow the creation of a new class(derived class) from an existing class(base class or super class)
	ex.:
		> class Animal {
			eat() function
			sleep() function
			
		};
		
		> class Dog :: public Animal {
			bark() function
			
		};
		
		> Dog rufus;
		> rufus.sleep()
			> the inheritance allow us to use a function from the base class in the derived class
			> in the example the 'dog' class can use the sleep() function from the base class
			
	> inheritance is an 'is-a relationship', is used only when an 'is-a relationship' is present
	> ex.:
		> a car is a vehicle
		> orange is a fruit
		> a surgeon is a doctor
		> a dog is an animal
		
	> protected members of a class can be accessed by an derived class unlike a private member
		> class Animal {
			protected:
				std::string type;
				
		};
		
		> class Dog : public Animal {
			public:
				void setType(std::string tp) {
					type = tp;
					
				}
				void displayType() {
					std::cout << "i am a " << type << std::endl;
				}
		};	
		
		int main() {
			Dog brutus;
			brutus.setType("german shepherd");
			brutus.displayType();
		
			return 0;
		}
		
	> access modes
	> is possible to derive class in various ways:
		> class Dog : public Animal {};
			> the derived class will inherite the members of the base class as they are if they are defined as 'public:'
			
		> class Dog : private Animal {};
			> all members of the base class will become 'private:' in the derived class
			
		> class Dog: protected Animal {};
			> the 'public:' members of the base class will become 'protected:' in the derived class
			
	> multlevel inheritance
	> is when a class is derived from an derived class
	> ex.:
		> class A {};
		> class B : public A {};
		> class C : public B {};
		
	> multiple inheritance
	> is when a class is derived from more than one base class
		> class Mammal {};
		> class WingedAnimal {};
		> class Bat : public Mammal, public WingedAnimal {};
		
	> ambiguity in multiple inheritance
	> occurs when a function is derived from both base class with the same name
	> ex.:
		> class Base1 {
			public:
				void someFunction() {}
		};
		
		> class Base2 {
			public:
				void someFunction() {}
		};
	
		> class Derived : public Base1, public base2 {};
		
		> int main() {
			Derived object;
			object.someFunction();
				> wil occur a erro in compilation because the compiler don't know wich function is supose to be called
				> an way to fix it is:
					> object.Base1::someFunction();
					> object.Base2::someFunction();
		}
	
	> hierarchical inheritance
	> occurs when more than one class is derived from the same base class
	> ex.:
		> class Animal {};
		> class Horse : public Animal {};
		> class Bat : public Animal {};
		> class Dog : public Animal {};
		> class Cat : public Animal {};
		
	> friend fuction
	> is an function that can access the private and protected member of a class
	> ex.:
		> class Distance {
			private:
				int meter;
				
				friend int addFive(Distance);
			public:
				Distance() : meter(0) {}
		};
		
		int addFive(Distance dist) {
			dist.meter += 5;
			return dist.meter;
		}
		
		int main() {
			Distance D;
			std::cout << "distance: " << addFive(D);
			return 0;
		}
		
	> friend class
	> a friend class can use all member of a base class 
	> ex.:
		> class ClassB;
		> class ClassA {
			friend class ClassB;
		};
		> class ClassB {};
		
[Virtual Function]
	> is an function created in the base class to be oberridden in the derived class
	> ex.:
		> class Base {
			public:
				virtual void print() {
					//code
				}
		};
		> class Derived : public Base {
			public:
				void print() {
					//code
				}
		};
		
		> int main() {
			Derived derived1;
		
			//pointer of Base type that point to derived1
			Base* base1 = &derived1;
			
			//call member function of derived class
			base1->print();
			
		}
		
[Libraries]
#<cstring>
	strlen	calculates the length of string
	strcat	Appends one string at the end of another
	strncat	Appends first n characters of a string at the end of another
	strcpy	Copies a string into another
	strncpy	Copies first n characters of one string into another
	strcmp	Compares two strings
	strncmp	Compares first n characters of two strings
	strchr	Finds first occurrence of a given character in a string
	strrchr	Finds last occurrence of a given character in a string
	strstr	Finds first occurrence of a given string in another string