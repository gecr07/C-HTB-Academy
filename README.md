# CSharp

Primeo que nada vamos a instalar para no instalar todo selecciona como en la imagen

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/94dd1702-ff0d-4e37-a855-b4e53b1ec6cf)

Plantilla basica para cualquier programa HelloWorld

```
using System;
class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello, World!");
    }
}
```

## Un Poco de Historia 

C# se anunció oficialmente en julio de 2000, seguido del lanzamiento de .NET Framework 1.0 en 2002. C# es uno de varios lenguajes que se pueden utilizar para crear aplicaciones .NET, pero con diferencia el más dominante. Se pueden utilizar otros lenguajes con .NET Framework, como Visual Basic y F#.


## Arquitectura

Es .NET Frameworkuna plataforma de ejecución y desarrollo de software independiente del idioma desarrollada por Microsoft. Proporciona un entorno controlado para desarrollar y ejecutar aplicaciones. Los programas escritos para .NET Framework se ejecutan en un entorno de software conocido como Common Language Runtime(CLR), una máquina virtual de aplicaciones que proporciona servicios como seguridad, administración de memoria y manejo de excepciones. Hay muchos componentes diferentes en .NET Framework; algunos se enumeran a continuación:

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/ca13ed82-eaed-43c7-adcd-d6d090beb535)


> Just-In-Time compilation aims to combine the benefits of both interpretation and static compilation. It translates the source code into an intermediate form, akin to bytecode, a portable, platform-independent code. The bytecode is closer to machine code than the high-level source code but is not tied to a specific hardware configuration.

Un compilador JIT es parte de Common Language Runtime( CLR). En lugar de crear código de máquina durante la compilación, .NET compila en un lenguaje intermedio llamado Microsoft Common Intermediate Language (MSIL o CIL). Luego, el procesador ejecuta este código de máquina. El CLR mantiene un caché de métodos compilados durante la ejecución del programa. Si se llama a un método más de una vez, CLR puede omitir el paso de compilación JIT en llamadas posteriores y usar el código de máquina previamente compilado, lo que genera mejoras de rendimiento.

## .NET Core y .NET

Microsoft lo presentó .NET Corecomo sucesor de .NET Framework, abordando muchas de las limitaciones y preocupaciones de .NET Framework, como que es específico de Windows y no es compatible con otras plataformas. .NET Core es un marco multiplataforma diseñado para crear aplicaciones modernas, basadas en la nube y conectadas a Internet. Se ejecuta en Windows, Linux y macOS, lo que lo convierte en una opción adecuada para los desarrolladores que buscan una amplia compatibilidad. .NET Core comprende CoreCLRun entorno de ejecución completo y CoreFXuna biblioteca creada para ejecutar aplicaciones. Fue lanzado por primera vez en junio de 2016.

> En 2020, Microsoft anunció que estaba consolidando sus ofertas .NET en una única plataforma .NET. Esto marcó el nacimiento de .NET 5, cuyo objetivo era unificar .NET Framework y .NET Core. El proceso de unificación se diseñó para aprovechar lo mejor de .NET Core, .NET Framework, Xamarin y Mono para crear una plataforma única para todas las aplicaciones .NET. El cambio tenía como objetivo proporcionar un único marco y tiempo de ejecución de .NET que se pueda utilizar en todas partes, fortaleciendo aún más la versatilidad y solidez de la plataforma .NET.

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/91b8aa3d-c6aa-4de9-9678-61fc69cb85d9)

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/d307d290-4c00-4e5f-b5f8-101efab8b7f4)


Otra plantilla basica 

```
class Program
{
    public static void Main()
    {
        // ...
    }
}
```


### Entry point (Main)

In C#, any application begins its execution from a special method known as Main. This is the entry point of any C# application. When the application starts, the Main method is the first invoked method. The C# compiler will show an error if the Main method is absent.

```
class Program
{
    public static void Main() { }
    public static int Main() { }
    public static int Main(string[] args) { }
    public static async Task Main() { }
    public static async Task<int> Main() { }
    public static async Task Main(string[] args) { }
    public static async Task<int> Main(string[] args) { }
    public static void Main(string[] args)
    {
        // Program execution starts here
    }
}
```

### Case Sensitivity

In C#, case sensitivity is a fundamental aspect of the language syntax. This means the language differentiates between uppercase and lowercase characters, treating them as distinct. As a result, identifiers named with different cases are considered separate entities by the C# compiler.

This feature extends to all areas of the language, including class names, method names, and other identifiers. For example:

### Semicolon

The semicolon (;) is known as a statement terminator in C#. It's employed to signify the end of a specific statement or command in the code. Using the semicolon as a statement terminator is common in many programming languages, including C++, Java, and JavaScript.

### Blocks of code 

Blocks in C# are sections of code enclosed in braces ({ }). They are typically used to group multiple statements together to form a single executable unit, such as the body of a method, loop, or conditional statement.

### comments

Como c ...

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/c38a6570-d744-48bb-9cac-5b9e71775785)

### Variables

Se asignan al estilo de C

### Constantes

Ya sabes una vez declarado su valor no se puede cambiar.

```
const int myConstant = 10;
```

### Enumeraciones 

Es como en C puedes escojer un tipo de dato pore jemplo de una semana podrias elegir los dias.

```
public enum Day 
{
    Sunday,
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday
}

```
Entonces el primer dia seria 0 y asi hasta llegar al sabado de nuevo que seria 6. Ojo tambien se puede poner numeros arbitrarios 

```
public enum Month : byte
{
    January = 1,
    February = 2,
    // And so on...
}
```

## C# Data types


```
byte aByte = 255; // Range: 0 to 255
sbyte aSbyte = -128; // Range: -128 to 127
short aShort = -32768; // Range: -32,768 to 32,767
ushort aUshort = 65535; // Range: 0 to 65,535
int anInt = -2147483648; // Range: -2,147,483,648 to 2,147,483,647
uint aUint = 4294967295; // Range: 0 to 4,294,967,295
long aLong = -9223372036854775808; // Range: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
ulong aUlong = 18446744073709551615; // Range: 0 to 18,446,744,073,709,551,615
float aFloat = 3.1415927f; // Range: ±1.5 x 10^-45 to ±3.4 x 10^38, Precision: 7 digits
double aDouble = 3.141592653589793; // Range: ±5.0 x 10^-324 to ±1.7 x 10^308, Precision: 15-16 digits
decimal aDecimal = 3.14159265358979323846m; // Range: ±1.0 x 10^-28 to ±7.9 x 10^28, Precision: 28-29 digits
bool aBool = true; // or false
char aChar = 'C'; // Can be a letter, a number, a symbol, or a special character like a newline (`\n`) or a tab (`\t`)
string aString = "Hello, World!";
```

En casos excepcionales, es posible que no conozca el tipo de variable en el momento de la compilación. Para tales casos, C# proporciona un tipo especial llamado var. La varpalabra clave indica al compilador que infiera el tipo de variable a partir de la expresión en el lado derecho de la declaración de inicialización. Luego, el compilador asigna el tipo más apropiado.

```
var number = 10; // The compiler will infer that 'number' is an integer
var message = "Hello, World!"; // Here, 'message' is inferred as a string


```

Es importante tener en cuenta que varsolo se puede utilizar cuando una variable se declara e inicializa simultáneamente. Una vez que una variable se declara vare inicializa, su tipo no se puede cambiar; permanece fuertemente tipado.

```
var myVariable = 10;
myVariable = "Hello"; // This will cause a compile error
int? nullableInt = null;
```

### Operadores

Aritmeticos ya sabes operadores de suma resta etc etc.

```
int a = 10;
int b = 5;

int sum = a + b; // Result: 15
int difference = a - b; // Result: 5
int product = a * b; // Result: 50
int quotient = a / b; // Result: 2
int remainder = a % b; // Result: 0
```

Operares relacionales mayor que menor que etc etc.

```
int a = 10;
int b = 20;

bool isEqual = (a == b); // Result: false
bool isNotEqual = (a != b); // Result: true
bool isGreaterThan = (a > b); // Result: false
bool isLessThan = (a < b); // Result: true
bool isGreaterThanOrEqualTo = (a >= b); // Result: false
bool isLessThanOrEqualTo = (a <= b); // Result: true
```

Operadores logicos and ir not

```
bool isTrue = true;
bool isFalse = false;

bool andResult = isTrue && isFalse; // Result: false
bool orResult = isTrue || isFalse; // Result: true
bool notResult = !isTrue; // Result: false
```

### Operadores a nivel de bits


They include & (bitwise AND), | (bitwise OR), ^ (bitwise XOR), ~ (bitwise NOT), << (left shift), and >> (right shift).

```
int a = 240; // Binary: 1111 0000
int b = 15; // Binary: 0000 1111

int andResult = a & b; // Result would be 0, Binary: 0000 0000
int orResult = a | b; // Result would be 255, Binary: 1111 1111
int xorResult = a ^ b; // Result would be 255, Binary: 1111 1111
int notResult = ~a; // Result would be -241, Binary: 0000 1111
int leftShift = a << 2; // Result would be 960, Binary: 11 1100 0000
int rightShift = a >> 2; // Result would be 60, Binary: 0011 1100
```

Operadores de asignacion son como los que acortan las cosas

```
int a = 10; // simple assignment

a += 5; // equivalent to a = a + 5, so a now is 15
a -= 3; // equivalent to a = a - 3, so a now is 12
a *= 2; // equivalent to a = a * 2, so a now is 24
a /= 4; // equivalent to a = a / 4, so a now is 6
a %= 5; // equivalent to a = a % 5, so a now is 1

```

Unary Operators Unary operators are those that operate on a single operand. They include ++ (increment), -- (decrement), + (unary plus, denotes positive values), and - (unary minus, denotes negative values). Unary operators also include the ! logical negation operator mentioned earlier.

```
int a = 5;
a++; // Now a is 6
a--; // Now a is 5 again
int b = +a; // b is 5
int c = -a; // c is -5

```

Ternary operators provide a shorthand way of writing an if-else condition. The syntax is condition ? true expression : false expression. if-else and other control flow statements are explained in Control Statements and Loops.

```
int a = 10;
int b = 20;

// expanded if-else
if (a > b)
{
    result = "a is greater";
}
else
{
    result = "b is greater";
}

// contracted ternary
string result = a > b ? "a is greater" : "b is greater";
```

### Null Conditional Operators

Estos operadores, introducidos en C# 6.0, se utilizan para acceder a miembros y elementos de un objeto de forma segura. Retornan nullsi el objeto es nullen lugar de arrojar un NullReferenceException.

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/af2a1df2-777d-4df0-9bb1-fc24a367131c)

```
string[] authors = null;
var author1 = authors?[0]; // This will not throw an exception even though authors is null. author1 will simply be null.

string authorName = null;
int? length = authorName?.Length; // Again, this will not throw an exception. length will be null.
```

### Null-coalescing Operator

> En C#, el signo de interrogación ? se utiliza para declarar una variable como "nullable" o "nulable". Una variable nullable es aquella que puede contener un valor o un valor nulo (null). En C#, algunos tipos de datos, como int, bool, float, etc., son tipos de valor y, por defecto, no pueden contener un valor nulo. Sin embargo, al agregar el signo de interrogación después del tipo de dato, estás indicando que la variable puede tener un valor nulo.

```
int? x = null;
int y = x ?? -1;
```

```
int? x = null;
int y;

if (x != null)
    y = x.Value;
else
    y = -1;
```
Otro ejemplo 

```
int? x = null;
x ??= -1;  // x is now -1 because it was null

```

## Type Conversion

Ya sabes convesion de tipos y existen 2 conversion explicita y conversion implicita.

```
int numInt = 10;
long numLong = numInt; // Implicit conversion from int to long
```

Explicita 

```
double numDouble = 10.5;
int numInt = (int)numDouble; // Explicit conversion from double to int. numInt will be 10, the fractional part is lost
```

C# also supports built-in methods for converting types, particularly from/to string types, like ToString(), ToInt32(), ToDouble(), etc., which are part of the Convert class.

El operador is It checks whether an object is compatible with a given type, and the result of the operation is bool.

```
string str = "Hello, World!";
bool result = str is string; // result will be true

```

AS operator It is used for casting between compatible reference types or nullable types. If the cast fails, it returns null instead of throwing an exception.

```
object obj = new string("Hello, World!");
string str = obj as string; // str will be "Hello, World!" if the cast is successful; otherwise, it will be null

```

### Namespaces

In C#, a namespace is a way to group related code elements into logical units, such as classes, interfaces, enums, and more. Namespaces provide organisation and help avoid naming conflicts by creating a hierarchical structure for code. They serve as containers for organising and categorising code elements, making managing and maintaining large codebases easier. Namespaces also enable code reuse and promote modularity by clearly separating concerns.

```
namespace MyNamespace
{
    class MyClass
    {
        // Class implementation
    }

    interface IMyInterface
    {
        // Interface implementation
    }
}
```


You have two options to use code elements from a namespace in a C# program: either fully qualify the code element's name with the namespace, or import the namespace via the using directive.

```
using System;

namespace MyNamespace
{
    class Program
    {
        static void Main()
        {
            // Using a fully qualified name
            System.Console.WriteLine("Hello, World!");

            // Using the imported namespace
            Console.WriteLine("Hello, World!");
        }
    }
}
```

Resolving Naming Conflicts with Namespaces 

Usando dodo el fully qualified name.

```
namespace MyNamespace
{
    class MyClass { }

    class Program
    {
        static void Main()
        {
            // Using fully qualified name to avoid naming conflict
            MyNamespace.MyClass myObject = new MyNamespace.MyClass();
        }
    }
}
```

Alias the Namespace: When importing, use an alias to differentiate between conflicting namespaces. This provides a shorthand way to refer to the code elements without ambiguity.


```
using MyAlias = MyNamespace;
using AnotherAlias = AnotherNamespace;

namespace MyNamespace
{
    class MyClass { }
}

namespace AnotherNamespace
{
    class MyClass { }

    class Program
    {
        static void Main()
        {
            // Using aliases to differentiate between conflicting namespaces
            MyAlias.MyClass myObject1 = new MyAlias.MyClass();
            AnotherAlias.MyClass myObject2 = new AnotherAlias.MyClass();
        }
    }
}
```

Entonces recuerda usa "using" para importar namespaces.

## Entrada y Salida

Para leer datos se utiliza Console.Read Cuando el usuario ingresa un carácter y presiona la tecla Intro, Console.Readrecupera el valor ASCII del carácter y lo devuelve como un número entero. Si se ha alcanzado el final del flujo de entrada, este método devolverá -1.

```
Console.Write("Please press a key: ");
int input = Console.Read();
Console.WriteLine("You pressed: " + (char)input);
```

Para cuando quieres leer mas de un solo caracter se utiliza Console.ReadLine

```
Console.Write("Please enter your name: ");
string name = Console.ReadLine();
Console.WriteLine("Hello, " + name);
```
Al presionar la tecla Intro, Console.ReadLinedevuelve la entrada capturada como una cadena. Si no hay más líneas disponibles (es decir, se alcanza el final del flujo de entrada), el método devolverá nulo.


Salida para imprimir texto en la pantall se utiliza Console.Write  This method does not append a trailing newline character to the output. As a consequence, any subsequent calls to Console.Write or Console.WriteLine will continue on the same line in the console.

```
Console.WriteLine("Hello, World!");
Console.WriteLine("Today's date is " + DateTime.Now.ToShortDateString());
```

## Control Statements

Ya sabes if else if

```
int number = 10;
if (number > 0) {
    Console.WriteLine("The number is positive.");
}
```

Else

```
int number = -10;
if (number > 0) {
    Console.WriteLine("The number is positive.");
}
else {
    Console.WriteLine("The number is not positive.");
}
```

```
int number = 0;
if (number > 0) {
    Console.WriteLine("The number is positive.");
}
else if (number < 0) {
    Console.WriteLine("The number is negative.");
}
else {
    Console.WriteLine("The number is zero.");
}
```

Ya despues esta el switch 

```
int number = 1;
switch (number) {
    case 1:
        Console.WriteLine("One");
        break;
    case 2:
        Console.WriteLine("Two");
        break;
    default:
        Console.WriteLine("None");
        break;
}

```

En este caso, la switchdeclaración evalúa el number. Coincide numbercon los casos y, si encuentra una coincidencia, ejecuta el código en ese bloque de casos. En el ejemplo anterior, imprimiría "Uno".

La breakdeclaración sirve para terminar la switchdeclaración. La ausencia del breakpuede provocar una caída en casos posteriores, lo que podría provocar resultados no deseados.

El defaultcaso dentro de una switchdeclaración define el bloque de código que se ejecutará en caso de que ningún otro caso coincida con el number. En el ejemplo, si el número no fuera ni 1 ni 2, se imprimiría "Ninguno".

```
for (int i = 0; i < 5; i++) {
    Console.WriteLine(i);
}
```
Esta es la sintaxis de  c

```
int i = 0;
while (i < 5) {
    Console.WriteLine(i);
    i++;
}
```
El do para hacer una condicion primero

```
int i = 0;
do {
    Console.WriteLine(i);
    i++;
} while (i < 5);
```

## Break, continue and goto

El break sirve para salirte de un loop por ejemplo para salirte del for.

```
for (int i = 0; i < 10; i++)
{
    if (i == 5)
    {
        break;
    }
    Console.WriteLine(i);
}
```

Continue se usa para skip el resto de instrucciones y continuar con el loop pero esa iteracion no la termina de ejecutar.

```

        for (int i = 0; i < 10; i++)
        {
            if (i == 5)
            {
                continue;
                Console.WriteLine("Esto no se va a ejecutar para cuando i sea 5 sin embargo todas las dema si");
            }
            Console.WriteLine(i);
        }

```

goto The goto statement transfers the program control directly to a labelled statement. A common use of goto is to transfer control from a nested loop to an outer loop or to exit deeply nested loops.

```

```

## Arrays

Se declaran tipo c

```
int [] array;
```

Para crear un arreglo ya en memoria usa la palabra new ( nada que no sepas del c)

```
array = new int[5];
int[] array = new int[] { 1, 2, 3, 4, 5 };
```
Ya sabes podemos declarar arreglos multidimensionales.

```
matrix = new int[3, 3];
int[,] matrix = new int[,] { { 1, 2, 3 }, { 4, 5, 6 }, { 7, 8, 9 } };
```

> 
El método GetLength(int dimension) se utiliza para obtener la longitud (número de elementos) de una dimensión específica en una matriz multidimensional en C#. Esta función es útil cuando trabajas con matrices que tienen más de una dimensión y deseas conocer la cantidad de elementos en una dimensión específica, ya sea la primera dimensión (índice 0) o la segunda dimensión (índice 1) en una matriz bidimensional, por ejemplo.

```
int[,] matrix = new int[,] { { 1, 2, 3 }, { 4, 5, 6 }, { 7, 8, 9 } };

// Use the GetLength method to get the number of rows (dimension 0) and columns (dimension 1)
for (int i = 0; i < matrix.GetLength(0); i++) {
    for (int j = 0; j < matrix.GetLength(1); j++)
    {
        // Access each element of the array using the indices
        Console.Write(matrix[i, j] + " ");
    }
    Console.WriteLine(); // Print a newline at the end of each row
}

```

Entonces la primera dimension es 0 y la segunda es 1 por eso imprime bien todo

### The array class

part of the System namespace. It provides various properties and methods like Length, Sort(), Reverse(), and many more that allow you to manipulate arrays.

```
int[] numbers = {8, 2, 6, 3, 1};
Array.Sort(numbers);
int[] numbers = {1, 2, 3};
Array.Reverse(numbers);
int[] numbers = {1, 2, 3};
int index = Array.IndexOf(numbers, 2);
//The variable index now holds the value 1, which is the index of number 2 in the array.


int[] numbers = {1, 2, 3};
Array.Clear(numbers, 0, numbers.Length);
//Now all elements in our array are set to zero: {0, 0, 0}.

```

## Strings

La principal diferenciación entre una cadena y una matriz de caracteres es que las cadenas en C# son inmutables, lo que significa que una vez creadas, no se pueden cambiar. Cualquier operación que parezca alterar la cadena en realidad crea una nueva cadena y descarta la anterior. Este diseño mejora la seguridad y mejora el rendimiento para texto estático o que rara vez cambia.

Por otro lado, las matrices de caracteres son mutables y los elementos individuales se pueden cambiar libremente. Esta mutabilidad tiene el costo de no tener métodos de comparación y manipulación de texto integrados, como lo hacen las cadenas.

```
//hay muchas operaciones que puede realizar en ella. La Lengthpropiedad, por ejemplo, devuelve el número de caracteres de la cadena.
string welcomeMessage = "Welcome to Academy!";
Console.WriteLine(welcomeMessage.Length); // Outputs: 19
// CONCATENACION

string firstString = "Welcome ";
string secondString = "to Academy!";
string concatenatedString = firstString + secondString;
Console.WriteLine(concatenatedString); // Outputs: "Welcome to Academy!"

```

Cuando se trata de manipular la estructura de cadenas, la Stringclase proporciona los métodos ToLowery ToUpper. ToLowerconvierte todos los caracteres de una cadena a minúsculas, mientras que ToUpperlos convierte todos a mayúsculas.

```
string lowerCaseString = welcomeMessage.ToLower();
Console.WriteLine(lowerCaseString); // Outputs: "welcome to academy!"

string upperCaseString = welcomeMessage.ToUpper();
Console.WriteLine(upperCaseString); // Outputs: "WELCOME TO ACADEMY!"


// También existen métodos para comprobar si una cadena comienza o termina con una subcadena específica. Estos son los métodos StartsWithy EndsWith, respectivamente.

bool startsWithWelcome = welcomeMessage.StartsWith("Welcome");
Console.WriteLine(startsWithWelcome); // Outputs: True

bool endsWithProgramming = welcomeMessage.EndsWith("Academy!");
Console.WriteLine(endsWithProgramming); // Outputs: True

```

Un requisito común en programación es determinar si existe una subcadena específica dentro de una cadena más grande. Esto se puede lograr con el Containsmétodo.

```
bool containsCsharp = welcomeMessage.Contains("C#");
Console.WriteLine(containsCsharp); // Outputs: False
```

A veces, es posible que necesite reemplazar todas las apariciones de una subcadena dentro de una cadena con otra subcadena. El Replacemétodo te permite hacer esto.

```
string replacedMessage = welcomeMessage.Replace("Academy", "HTB Academy");
Console.WriteLine(replacedMessage); // Outputs: "Welcome to HTB Academy!"

```

Puede utilizar el Equalsmétodo o el ==operador al comparar dos cadenas para determinar la igualdad. Ambos realizan una comparación que distingue entre mayúsculas y minúsculas de forma predeterminada.

```
string str1 = "Welcome";
string str2 = "welcome";
bool areEqual = str1.Equals(str2);
Console.WriteLine(areEqual); // Outputs: False
```

## Interpolacion de cadenas (como en bash ${var})

Para crear una cadena interpolada en C#, anteponga la cadena con un $símbolo y escriba cualquier variable o expresión que desee interpolar entre llaves {}. Cuando se procesa la cadena, estas expresiones se reemplazan por sus representaciones de cadena evaluadas.

```
string name = "Alice";
string greeting = $"Hello, {name}!";
Console.WriteLine(greeting); // Outputs: "Hello, Alice!"
```

### Trim

Otra operación importante de la cuerda es el recorte, que se realiza mediante el Trimmétodo. Esto se usa comúnmente para eliminar los espacios en blanco iniciales y finales de una cadena.

```
string paddedString = "    Extra spaces here    ";
string trimmedString = paddedString.Trim();
Console.WriteLine(trimmedString); // Outputs: "Extra spaces here"
```

### Substring 

Extrae una parte de la cadena.

```
string fullString = "Hello, World!";
string partialString = fullString.Substring(7, 5); // empiza desde el 0
Console.WriteLine(partialString); // Outputs: "World"
```


### Split 

Además, utilizando el Splitmétodo, las cadenas se pueden dividir en matrices de subcadenas basadas en delimitadores. Esto es especialmente útil al analizar entradas o manejar datos que vienen en forma de cadena.


```
string sentence = "This is a sentence.";
string[] words = sentence.Split(' ');
foreach (string word in words) // Mira esta sintaxis de powershell al parecer
{
    Console.WriteLine(word);
}
// Outputs: 
// "This"
// "is"
// "a"
// "sentence."

```

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/50ef0417-67ae-4eda-b212-4bdbf8ee433a)


### Join 


```
string[] words = { "This", "is", "a", "sentence" };
string sentence = string.Join(" ", words);
Console.WriteLine(sentence); // Outputs: "This is a sentence"
```

Ejercicio de Reverse the string 

```
        string message = "...semit egnartS ?thgir drieW...seludom ymedacA setirw neht dna god yzal eht revo spmuj xof nworb kciuq ehT";
        char[] charArray = message.ToCharArray();
        Array.Reverse(charArray);
        string a10 = new string(charArray);
        Console.WriteLine(a10); 

```

## Collections

In C#, a collection is used to group related objects. Collections provide a more flexible way to work with groups of objects, as unlike arrays, the group of objects you work with can grow and shrink dynamically as the demands of the application change. Collections are defined in the System.Collections namespace.

### Iterar sobre los objetos 

The foreach loop is an efficient and straightforward way to iterate through any collection. It automatically moves to the next item in the collection at the end of each loop iteration, making it an excellent choice for reading collections. Suppose you want to modify the collection while iterating over it. In that case, you might need to use a different looping construct, like a for loop, as foreach does not support collection modification during iteration.


```
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };

for (int i = 0; i < numbers.Count; i++)
{
    // Modify the element at index i
    numbers[i] *= 2;
}

foreach (int number in numbers)
{
    Console.WriteLine(number);
}

```

### List 

A List<T> is one of the most commonly used types in .NET, especially when we need a resizable array-like collection. This type is found in the System.Collections.Generic namespace is a generic class which supports storing values of any type. However, all List<T> elements must be the same type.

```
List<string> namesList = new List<string>();

// Adding elements to the list
namesList.Add("John");
namesList.Add("Jane");
namesList.Add("Alice");

// Accessing elements by index
string firstElement = namesList[0]; // O(1) indexed access

// Modifying an element
namesList[1] = "Emily";

// Checking if an element exists
bool hasAlice = namesList.Contains("Alice");

// Removing an element
namesList.Remove("John");

// Iterating over the elements
foreach (string name in namesList)
{
    Console.WriteLine(name);
}
```

A List<T> provides the advantage of dynamic resizing compared to an array. However, this also means that a List<T> generally uses more memory than an array, as it allocates extra space to allow for potential growth. If the size of your collection is fixed, using an array could be more memory-efficient.

However, the flexibility and utility of the List<T> class methods often outweigh the minor performance and memory usage benefits of arrays in many scenarios. This is especially true in applications where the exact count of elements may change over time.

### Dictionary

A Dictionary<TKey, TValue> is a collection that stores and retrieves data using a key-value relationship. It is part of the System.Collections.Generic namespace in C#.

To use a Dictionary<TKey, TValue>, specify the key type (TKey) and the value (TValue) in the angle brackets. For example, Dictionary<int, string> indicates a dictionary where the keys are integers and the values are strings.

```
Dictionary<string, int> studentGrades = new Dictionary<string, int>();

// Adding key-value pairs to the dictionary
studentGrades.Add("John", 85);
studentGrades.Add("Jane", 92);
studentGrades.Add("Alice", 78);

// Accessing values by key
int johnGrade = studentGrades["John"]; // O(1) lookup by key

// Modifying an existing value
studentGrades["Jane"] = 95;

// Checking if a key exists
bool hasAlice = studentGrades.ContainsKey("Alice");

// Removing a key-value pair
studentGrades.Remove("John");

// Iterating over the key-value pairs
foreach (KeyValuePair<string, int> pair in studentGrades)
{
    Console.WriteLine($"Name: {pair.Key}, Grade: {pair.Value}");
}
```

### HashSet

A HashSet<T> collection stores an unordered set of unique elements. The primary characteristic of a HashSet is its ability to store unique elements, completely disallowing duplication. Adding elements to a HashSet will check if the element already exists before adding it. This makes HashSet an optimal choice when you need to store a collection of items without any duplicates and do not require a specific order.

```
HashSet<string> namesHashSet = new HashSet<string>();

// Adding elements to the set
namesHashSet.Add("John");
namesHashSet.Add("Jane");
namesHashSet.Add("Alice");

// Checking if an element exists
bool hasAlice = namesHashSet.Contains("Alice"); // O(1) membership check

// Removing an element
namesHashSet.Remove("John");

// Iterating over the elements
foreach (string name in namesHashSet)
{
    Console.WriteLine(name);
}
```

## LINQ (consulta integrada de lenguaje)

Language Integrated Query (LINQ) es una característica de C# que proporciona un modelo coherente para trabajar con datos en varios tipos de fuentes y formatos de datos. Utilice LINQ para consultar datos con C# independientemente de la fuente de datos.

En un sentido más técnico, LINQ es un conjunto de métodos, proporcionados como métodos de extensión en .NET, que proporcionan un enfoque universal para consultar datos de cualquier tipo. Estos datos pueden ser objetos en memoria (como listas o matrices), XML, bases de datos o cualquier otro formato para el que esté disponible un proveedor LINQ. Estos métodos toman expresiones lambda como argumentos, que se comportan como funciones en línea que funcionan en el conjunto de datos que se consulta.

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/4ce74abd-6b1f-4104-bfe3-b704f10265b9)

LINQ proporciona dos sintaxis principales para escribir consultas: sintaxis de consulta y sintaxis de método. A menudo se prefiere la sintaxis de consulta por su legibilidad y parecido con SQL, mientras que la sintaxis del método ofrece más flexibilidad y capacidad de composición. Exploremos ambas sintaxis con ejemplos.

Ejemplo sintaxis de consulta.
```
// This creates a new list of integers named 'numbers' and populates it with the numbers from 1 to 10.
List<int> numbers = new List<int> { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };

// This is a LINQ query that will create a new collection called 'evenNumbers'. 
// The 'from num in numbers' part signifies that we're querying over the 'numbers' list and will refer to each element as 'num'.
// The 'where num % 2 == 0' part is a condition that each number in the list must satisfy to be included in the new collection - in this case, the number must be even. 
// The '%' operator is the modulus operator, which gives the remainder of integer division. So 'num % 2' gives the remainder when 'num' is divided by 2. If this remainder is 0, then the number is even.
// The 'select num' part signifies that if a number satisfies the condition, then it should be included in the 'evenNumbers' collection.
var evenNumbers = from num in numbers
                  where num % 2 == 0
                  select num;
```

Sintaxis ejemplo de sintaxis metodo.

```
// This creates a new list of integers named 'numbers' and populates it with the numbers from 1 to 10.
List<int> numbers = new List<int> { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };

// This is a LINQ query using method syntax. It creates a new collection called 'evenNumbers' from the 'numbers' list.
// The 'Where' method filters the 'numbers' list based on the provided lambda expression 'num => num % 2 == 0'.
// The lambda expression takes each number 'num' in the 'numbers' list and returns true if 'num' is even (i.e., if the remainder when 'num' is divided by 2 is 0), and false otherwise.
// The 'Where' method then includes in 'evenNumbers' only those numbers for which the lambda expression returned true.
// As a result, 'evenNumbers' will include all even numbers from the original 'numbers' list. The output will be: 2, 4, 6, 8, 10.
var evenNumbers = numbers.Where(num => num % 2 == 0); // Output: 2, 4, 6, 8, 10

```

Ahora utilizando el operador select

```
List<string> names = new List<string> { "John", "Alice", "Michael" };

// This line uses a LINQ query with the Select method to create a new collection 'upperCaseNames'. 
// The query takes the 'names' collection and applies the 'ToUpper' method to each element. 
// The ToUpper method is a built-in C# method that converts all the characters in a string to uppercase.
// The result is a new collection where all the names from the original 'names' collection are transformed into uppercase.
var upperCaseNames = names.Select(name => name.ToUpper());

// Output: JOHN, ALICE, MICHAEL
foreach (var name in upperCaseNames)
{
    Console.WriteLine(name);
}
```
Order by

```
List<int> numbers = new List<int> { 5, 2, 8, 1, 9 };

// The OrderBy method is a LINQ operation that sorts the elements of a collection in ascending order according to a key. In this case, the key is the numbers themselves.
var sortedNumbersAsc = numbers.OrderBy(num => num);

// Output: 1, 2, 5, 8, 9
foreach (var num in sortedNumbersAsc)
{
    Console.WriteLine(num);
}

// The OrderByDescending method is similar to OrderBy, but sorts the elements in descending order. Like in the previous example, the key is the numbers themselves.
var sortedNumbersDesc = numbers.OrderByDescending(num => num);

// Output: 9, 8, 5, 2, 1
foreach (var num in sortedNumbersDesc)
{
    Console.WriteLine(num);
}
```


Existen mas cosas que se pueden hacer pero considero que no lo usaras si se usa ya sabes como se llama y lo investigas.

### Aggregate 

```
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };

// This line uses the LINQ Aggregate method to generate a single value from the 'numbers' collection.
// The Aggregate method applies a specified function to the first two elements of the collection, then to the result and the next element, and so on. 
// In this case, the function is a lambda expression '(acc, num) => acc + num', where 'acc' represents the accumulated value so far and 'num' represents the current element.
// So essentially, this code sums up all the numbers in the 'numbers' collection. The resulting sum is then stored in the 'sum' variable.
var sum = numbers.Aggregate((acc, num) => acc + num);

// Output: 15
Console.WriteLine(sum);
```

## Methods and Exception handling

En C#, una declaración de método especifica el nombre del método, el tipo de retorno y los parámetros dentro de la definición de clase.

```
public int Multiply(int a, int b) 
{
    return a * b;
}
```

En C#, los términos "declaración" y "definición" de un método no suelen estar diferenciados, como sí lo están en algunos lenguajes como C o C++. Esto se debe a que C# no permite la declaración y definición de métodos por separado: cuando declara un método, también debe proporcionar su implementación, definiéndolo efectivamente.

Un staticmétodo pertenece a la clase misma y no a ninguna instancia de clase específica. Se declara con la palabra clave static.

```
public class MyClass
{
    // Static method
    public static void MyStaticMethod()
    {
        Console.WriteLine("This is a static method.");
    }
}

public class Program
{
    public static void Main(string[] args)
    {
        // Call the static method
        MyClass.MyStaticMethod();  // Outputs: This is a static method.
    }
}
```

Dado que los métodos estáticos están vinculados a la clase misma, solo pueden acceder a los otros miembros estáticos de la clase (métodos, propiedades, etc.). No pueden acceder a miembros no estáticos ya que pertenecen a instancias específicas de la clase.

Un método non-static(o instance) pertenece a una instancia de clase particular. Se declara sin utilizar la staticpalabra clave.

```
public class MyClass
{
    // Non-static (instance) method
    public void MyInstanceMethod()
    {
        Console.WriteLine("This is an instance method.");
    }
}

public class Program
{
    public static void Main(string[] args)
    {
        // Create an instance of MyClass
        MyClass myObject = new MyClass();

        // Call the instance method
        myObject.MyInstanceMethod();  // Outputs: This is an instance method.
    }
}

```
Para llamar a un método no estático, debes crear una instancia de la clase.

Instance methods can access the class's static and non-static members since they belong to a specific class instance.Static members can also include fields, properties, events, operators, and constructors.

## Exeptions

A try block is used to encapsulate a region of code. If any statement within the try block throws an exception, that exception will be handled by the associated catch block.

```
try
{
    // Code that could potentially throw an exception.
}
```

The catch block is used to catch and handle an exception. It follows a try block or another catch block. Each try block can have multiple catch blocks associated with it, each designed to handle specific or multiple exceptions. A catch block without a specified type will catch all exceptions.

```
catch (Exception ex)
{
    // Handle the exception
}
```

Un finallybloque le permite ejecutar código después de que se haya completado un bloque de prueba, independientemente de si se ha producido una excepción. Es opcional y limpia los recursos dentro del bloque try (como conexiones de bases de datos, archivos o recursos de red).

```
finally
{
    // Code to be executed after the try block has completed,
    // regardless of whether an exception was thrown.
}
```



Aqui tienes un ejemplo de todo junto 

```

try
{
    // Code that could potentially throw an exception.
    int divisor = 0;
    int result = 10 / divisor;
}
catch (DivideByZeroException ex)
{
    // Handle the DivideByZeroException.
    Console.WriteLine("Cannot divide by zero");
}
finally
{
    // Code to be executed after the try block has completed,
    // regardless of whether an exception was thrown.
    Console.WriteLine("This code is always executed.");
}
```

Cuando trate con catch blocks, recuerde que pueden manejar múltiples excepciones. El orden en el que se especifican los diferentes bloques catch es importante; se examinan de arriba a abajo, por lo que se ejecutará el primero que coincida con el tipo de excepción. Si tiene un bloque catch que maneja todas las excepciones en la parte superior, capturará todas las excepciones y ninguno de los bloques catch debajo se ejecutará. Esta es la razón por la que el bloque catch para el tipo de excepción más general, Exceptionsuele ser el último.


```
try
{
    // Code that could throw an exception
    int[] arr = new int[5];
    arr[10] = 30; // This line throws an IndexOutOfRangeException.
}
catch (IndexOutOfRangeException ex)
{
    // Handle specific exception first
    Console.WriteLine("An IndexOutOfRangeException has been caught: " + ex.Message);
}
catch (Exception ex)
{
    // General exception catch block
    Console.WriteLine("An exception has been caught: " + ex.Message);
}
```


El finallybloque se ejecuta independientemente de si se lanza una excepción. Si tiene algún código que deba ejecutarse, ya sea que se produzca una excepción o no, debe colocarse en un bloque finalmente. Por ejemplo, si abre un archivo en un bloque try, debe cerrarlo en un bloque finalmente, independientemente de si se produce o no una excepción al trabajar con el archivo.

```
StreamReader reader = null;
try
{
    reader = new StreamReader("file.txt");
    // Code to read the file.
}
catch (FileNotFoundException ex)
{
    Console.WriteLine(ex.Message);
}
finally
{
    // Whether an exception is thrown or not, close the file.
    if (reader != null)
        reader.Close();
}
```

### throw

The throw keyword can be used to raise exceptions. You can throw a pre-existing exception, or you can instantiate a new exception and throw it.

```
try
{
    // Throw a new exception.
    throw new Exception("A problem has occurred.");
}
catch (Exception ex)
{
    // Handle the exception.
    Console.WriteLine(ex.Message);
}

```
Puedes usar para tu poner tus propias exepciones ( quiza sea mejor usar las que ya esten definidas para hacer el codigo mas facil)

## Lambda Expressions

Una expresión lambda es un método sin nombre que calcula y devuelve un valor único. Son métodos simples de representar anonymous methods(métodos sin nombre) o functionsen línea.

Una expresión lambda consta de tres partes principales: a parameter list, lambda operator( =>) y an expression or statement. La sintaxis general de una expresión lambda se parece a esta:

```
(parameters) => expression or statement block

```

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/50854c80-1a25-45c8-b6ff-7c430ebf1dae)

```
var evenNumbers = numbers.Where(num => num % 2 == 0); // Output: 2, 4, 6, 8, 10
```

## Libraries 

C# includes many predefined functions and libraries that developers can use to accomplish various tasks more easily and efficiently. The .NET Framework provides these libraries and includes functionalities for things like file I/O, database access, networking, and much more.

A library in C# is typically provided as a .dll (Dynamic Link Library) file. To use the library's functions and classes, you must first reference it in your project. This will be done automatically if the library is installed via a package manager like nuget, or if you use a library from within the .NET ecosystem.

The using directive then tells the compiler to use a specific namespace in the library. A namespace groups related class, structures, and other types under a single name. For instance, the System namespace includes fundamental classes and base types that are used in C# programming.

For example, to use the File class from the System.IO namespace for handling files, you would first need to add using System.IO; at the top of your code.

```

using System.IO;

class Program
{
    static void Main(string[] args)
    {
        // Check if a file exists
        if (File.Exists("test.txt"))
        {
            // Read the content of the file
            string content = File.ReadAllText("test.txt");
            Console.WriteLine(content);
        }
        else
        {
            Console.WriteLine("The file does not exist.");
        }
    }
}
```

Similarly, you can use predefined functions from other namespaces and libraries—for instance, the System.Math namespace contains mathematical functions such as Math.Sqrt for computing the square root of a number, Math.Pow for raising a number to a specified power, and Math.Round for rounding a number to the nearest integer.


```
using System;

class Program
{
    static void Main(string[] args)
    {
        double num = 9.0;
        double squareRoot = Math.Sqrt(num);
        Console.WriteLine($"The square root of {num} is {squareRoot}");

        double baseNum = 2.0;
        double exponent = 3.0;
        double power = Math.Pow(baseNum, exponent);
        Console.WriteLine($"{baseNum} raised to the power of {exponent} is {power}");

        double toBeRounded = 9.5;
        double rounded = Math.Round(toBeRounded);
        Console.WriteLine($"{toBeRounded} rounded to the nearest integer is {rounded}");
    }
}
```

## NuGet

In addition to the standard libraries, C# offers extensive support for using third-party libraries and packages. These can be added to your project through various means, including the NuGet package manager. NuGet is a free and open-source package manager designed for the Microsoft development platform, and it hosts thousands of libraries.

Adding a NuGet package to your project can be as easy as right-clicking on your project in the Solution Explorer in Visual Studio, selecting "Manage NuGet Packages..." and then searching for and installing the required package. If using a code editor, we use the dotnet package add command, but Microsoft provides great documentation for using nuget from the CLI.

Once a package is installed, you can utilise its functionality in your code by adding the appropriate using directive at the top of your file. The Newtonsoft.Json package, for instance, provides powerful tools for working with JSON data.

```

using Newtonsoft.Json;
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        string json = "[{'Name':'John', 'Age':30}, {'Name':'Jane', 'Age':28}]";

        List<Person> people = JsonConvert.DeserializeObject<List<Person>>(json);

        foreach (var person in people)
        {
            Console.WriteLine($"Name: {person.Name}, Age: {person.Age}");
        }
    }
}

public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}

```

In this example, the JsonConvert.DeserializeObject<T> method is used to parse the JSON string into a list of Person objects. This predefined function, part of the Newtonsoft.Json library, dramatically simplifies the task of JSON parsing.

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/f829404e-0ff2-4424-9d4d-87b017cd4b07)

Para agregar la dependecia es ahi luego elijes el archivo DLL. Y para usarla:

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/4cfddff7-2487-4863-8602-bcc8d14de573)


![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/b2a4c4a1-bed4-41c8-ac3d-5e0bacc55132)

## POO Object-Oriented Programming

La Programación Orientada a Objetos (POO) es un paradigma de programación que se basa en el concepto de "objetos". Los objetos son instancias de clases, que pueden contener datos en forma de campos, a menudo conocidos como atributos, y código, en forma de métodos. En OOP, los programas de computadora se diseñan haciéndolos a partir de objetos que interactúan entre sí.

Hay cuatro principios fundamentales de la programación orientada a objetos:

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/83a14bdf-09c2-4e58-a798-26212afa9670)


```
class Car
{
    // Properties
    public string Color;
    public int Year;

    // Method
    public void Drive()
    {
        Console.WriteLine($"The {Color} car from {Year} is driving.");
    }
}
```

Para instanciar una clase

```
Car myCar = new Car();
```
Ejemplo de un constructor 

```
class Car
{
    // Properties
    public string Color;
    public int Year;
    
    // Constructor
    public Car(string c, int y)
    {
        Color = c;
        Year = y;
    }

    // Method
    public void Drive()
    {
        Console.WriteLine($"The {Color} car from {Year} is driving.");
    }
}
```

### Accessors

An accessor is a class member function that provides access to the value of private or protected data members. There are two types of accessors - get and set.

```
class Circle
{
    private double radius;

    public double Radius
    {
        get
        {
            return radius;
        }
    }
}
```
Entiendo que aqui el set y get se hacen asi a diferencia de JAVA:

```
class Circle
{
    private double radius;

    public double Radius
    {
        get
        {
            return radius;
        }
        set
        {
            if (value > 0)
                radius = value;
            else
                Console.WriteLine("Radius cannot be negative or zero");
        }
    }
}
```
Automatic properties 

```
class Circle
{
    private double radius;

    public double Radius
    {
        get
        {
            return radius;
        }
        set
        {
            radius = value;
        }
    }
}
```

Pero tambien se puede:

```
class Circle
{
    public double Radius { get; set; }
}
```

En este ejemplo, Radiuses una propiedad automática. La { get; set; }sintaxis le dice a C# que genere automáticamente un campo de respaldo oculto detrás de escena. Este campo almacena los datos reales y los descriptores de acceso gety setse utilizan para leer y escribir en este campo.

```
Circle c = new Circle();
c.Radius = 12345.54321;

Console.WriteLine(c.Radius);  // Outputs: 12345.54321

```

## Struct

A struct, abreviatura de estructura, es un tipo de valor en C#. Esto significa que cuando structse crea a, la variable a la que se asigna la estructura contiene los datos reales de la estructura. Esto contrasta con los tipos de referencia, donde la variable hace referencia a los datos del objeto, no a los datos reales en sí.

```
public struct Point
{
    public int X { get; set; }
    public int Y { get; set; }

    public Point(int x, int y)
    {
        X = x;
        Y = y;
    }
}


```

En este ejemplo, Pointes una estructura que representa un punto en un espacio bidimensional. Incluye dos propiedades ( Xy Y) y un constructor que inicializa esas propiedades.


La enczpsulacion. En C#, la encapsulación de datos se logra mediante modificadores de acceso, que controlan la visibilidad y accesibilidad de clases, métodos y otros miembros. Los modificadores de acceso clave son public, private, protectedy internal.


```
public class Employee
{
    // Private member data (fields)
    private string name;
    private int age;

    // Public getter and setter methods (properties)
    public string Name
    {
        get { return name; }
        set { name = value; }
    }

    public int Age
    {
        get { return age; }
        set 
        { 
            if(value > 0)
                age = value; 
            else 
                Console.WriteLine("Invalid age value");
        }
    }
}
```

> En este ejemplo, la Employeeclase encapsula los campos namey age. Estos campos son private, por lo que no se puede acceder a ellos directamente desde fuera de la Employeeclase. En cambio, el acceso se proporciona a través de las publicpropiedades Namey Age, que sirven como interfaz para la Employeeclase. Tenga en cuenta que el Ageconfigurador incluye lógica de validación para garantizar que no se pueda establecer una edad no válida. Este es un excelente ejemplo de encapsulación que protege los datos de un objeto. Los datos (en este caso, el age) están protegidos y encapsulados dentro de la Employeeclase.


### Herencia única

En la herencia única, una clase (también conocida como clase derivada o hija) hereda de una clase monoparental (también conocida como base o superclase). Esto permite que la clase derivada reutilice (o herede) los campos y métodos de la clase base, así como también introduzca otros nuevos.

```
public class Vehicle {
    public string color;
    
    public void Start() {
        Console.WriteLine("Vehicle started");
    }
}

public class Car : Vehicle {
    public string model;
    
    public void Drive() {
        Console.WriteLine("Driving car");
    }
}
``` 

Herencia multi nivel 

```
public class SportsCar : Car {
    public int topSpeed;
    
    public void TurboBoost() {
        Console.WriteLine("Turbo boost activated");
    }
}
```
En este caso, SportsCares una clase derivada que hereda de la Carclase, que a su vez hereda de la Vehicleclase. Esto significa que SportsCartiene acceso al colorcampo y Start()método de Vehicle, al modelcampo y Drive()método de Car, y también define su propio campo topSpeedy método TurboBoost().

Recuerde que C# no admite herencia múltiple, lo que significa que una clase no puede heredar directamente de más de una clase en el mismo nivel. Sin embargo, como hemos visto aquí, admite múltiples niveles de herencia y permite que una clase implemente múltiples interfaces. 

```
public class Vehicle
{
    public string Color { get; }

    public Vehicle(string color)
    {
        this.Color = color;
    }

    public void DisplayColor()
    {
        Console.WriteLine($"Color: {this.Color}");
    }
}

public class Car : Vehicle
{
    public string Brand { get; }

    public Car(string color, string brand) : base(color)
    {
        this.Brand = brand;
    }

    public void DisplayCarInformation()
    {
        base.DisplayColor();
        Console.WriteLine($"Brand: {this.Brand}");
    }
}
```

Aqui se usa base para llamar al metodo de la clase padre

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/cccc2d35-0f13-46bd-85b3-459cf1db9746)

### Polymorphism

In C#, polymorphism is generally realised through method overloading and overriding. Method overloading, also known as static or compile-time polymorphism, is a technique that allows multiple methods with the same name but different parameters (in terms of number, type, or order) to coexist within a class.


```
public class Mathematics
{
    public int Add(int a, int b)
    {
        return a + b;
    }

    public double Add(double a, double b)
    {
        return a + b;
    }
}
```

Existe 2 maneras de hacer esto:

#### Method Overloading
Method overloading, also known as static or compile-time polymorphism, is a technique that allows multiple methods with the same name but different parameters (in terms of number, type, or order) to coexist within a class.

#### Method Overriding
Method overriding, on the other hand, is a form of dynamic or run-time polymorphism. It allows a derived class to provide a different implementation for a method already defined in its base class or one of its base classes. The method in the base class must be marked with the virtual keyword, and the method in the derived class must use the override keyword.


```
public class Animal
{
    public virtual void MakeSound()
    {
        Console.WriteLine("The animal makes a sound");
    }
}

public class Dog : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("The dog barks");
    }
}
```
In the above example, the Dog class overrides the MakeSound method of the Animal class. When MakeSound is called on an object of type Dog, the overridden version in the Dog class is executed.

The concepts of overloading and overriding extend to operators and properties, adding flexibility and expressiveness to C# programming.

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/16d246a0-147f-4dc1-8af3-185eace321c4)

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/1d46f68b-ad1b-45a7-8121-879003194c15)

```
Dog myDog = new Dog("Rex");
Console.WriteLine(myDog.Name);  // "Rex the dog"
```

### Abstracción

En la programación orientada a objetos, la abstracción es el concepto de simplificar una realidad compleja modelando clases apropiadas para el problema y trabajando en el nivel de herencia más apropiado para un aspecto determinado del problema. Es un mecanismo que representa las características esenciales sin incluir los detalles de fondo.

La abstracción en C# se logra mediante el uso abstractde clases y interfaces. Una abstractclase es una clase de la que no se pueden crear instancias y normalmente se utiliza como clase base para otras clases. AbstractLas clases pueden tener abstractmétodos que se declaran en la abstractclase y se implementan en las clases derivadas.

```
public abstract class Animal
{
    public abstract void Speak();
}

public class Dog : Animal
{
    public override void Speak()
    {
        Console.WriteLine("The dog barks");
    }
}

public class Cat : Animal
{
    public override void Speak()
    {
        Console.WriteLine("The cat meows");
    }
}
```

El uso de la abstracción Interfaceses otra forma de lograr la abstracción. An interfacees como una abstractclase sin implementación. Solo declara los métodos y propiedades pero no contiene ningún código. Una clase que implementa una interfaz debe proporcionar una implementación para todos los métodos de la interfaz.


```
public interface IAnimal
{
    void Speak();
}

public class Dog : IAnimal
{
    public void Speak()
    {
        Console.WriteLine("The dog barks");
    }
}

public class Cat : IAnimal
{
    public void Speak()
    {
        Console.WriteLine("The cat meows");
    }
}
```

En este ejemplo, IAnimalhay una interfaz con un método Speak. Las clases Dogimplementan Caty IAnimalproporcionan su propia implementación de Speak.

En ambos ejemplos, el usuario no necesita entender cómo habla cada animal; sólo necesitan saber que todos los animales pueden hablar. Ésta es la esencia de la abstracción. Le permite concentrarse en lo que hace el objeto en lugar de cómo lo hace.


## Clases genéricas

Una declaración de clase genérica se parece mucho a una declaración de clase no genérica, excepto que una lista de parámetros de tipo entre corchetes angulares sigue al nombre de la clase. Los parámetros de tipo se pueden usar en el cuerpo de la clase como marcadores de posición para los tipos especificados cuando se crea una instancia de la clase.


```
public class GenericList<T>
{
    private T[] elements;
    private int count = 0;

    public GenericList(int size)
    {
        elements = new T[size];
    }

    public void Add(T value)
    {
        elements[count] = value;
        count++;
    }

    public T GetElement(int index)
    {
        return elements[index];
    }
}
```
En el ejemplo anterior, Tes el parámetro de tipo. Se puede crear una instancia de esta GenericListclase con cualquier tipo.

```
var list1 = new GenericList<int>(10);
var list2 = new GenericList<string>(5);
```
Métodos genéricos. Los métodos genéricos son métodos que se declaran con parámetros de tipo. Al igual que las clases genéricas, puede crear un método que posponga la especificación de uno o más tipos hasta que se llame al método.


![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/18d6bc28-ebf7-4554-87ab-31a38fa8d625)

## Asynchronous Programming

Asynchronous programminges una técnica poderosa en el desarrollo de software moderno que permite que los programas perform non-blocking operationsutilicen de manera eficiente los recursos del sistema. Permite que las aplicaciones handle time-consuming tasks without blocking the main execution threadmejoren la capacidad de respuesta y la escalabilidad.

Los métodos asincrónicos devuelven un objeto Tasku Task<T>que representa una operación en curso. El código de llamada puede continuar su ejecución mientras la operación asincrónica avanza en segundo plano. Una vez que se completa la operación, el resultado se puede recuperar o procesar más.

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/b80f3f27-7525-470e-a3bb-4c3f784289df)

En C#, la programación asincrónica se ve facilitada por las palabras clave asyncy await. La asyncpalabra clave se utiliza para especificar que un método, expresión lambda o método anónimo es asincrónico. Estos métodos suelen devolver un objeto Tasku Task<T>, que representa el trabajo en curso.

Por otro lado, la awaitpalabra clave se utiliza en un asyncmétodo para suspender la ejecución del método hasta que se complete una tarea en particular; el programa está awaiting Task<T>finalizado. awaitsólo se puede utilizar en un asyncmétodo.

(la awaitpalabra clave antes de una tarea para especificar que el método no puede continuar hasta que se complete la tarea esperada; mientras tanto, el control regresa a la persona que llama al método.)

```
async Task<T> MethodName()
{
    //...Method body
    await SomeTask;
    //...Continue after SomeTask finishes
}
```

```
public async Task<int> CalculateSumAsync(int a, int b)
{
    await Task.Delay(500); //Simulate some delay
    return a + b;
}

public async void CallCalculateSumAsync()
{
    int result = await CalculateSumAsync(5, 6);
    Console.WriteLine($"The sum is {result}");
}
```
Consideremos un ejemplo en el que llamamos a un servicio web para recuperar datos. Obtener datos de un servicio web puede llevar mucho tiempo, por lo que usaremos asyncy awaitpara asegurarnos de que nuestra aplicación siga respondiendo durante esta operación.

```
using System.Net.Http; // Network I/O is explained in more detail on the related page
using System.Threading.Tasks;

class Program
{
    static readonly HttpClient client = new HttpClient();

    static async Task Main()
    {
        string responseBody = await GetWebsiteContentAsync("http://example.com");

        Console.WriteLine(responseBody);
    }

    static async Task<string> GetWebsiteContentAsync(string url)
    {
        HttpResponseMessage response = await client.GetAsync(url);
        response.EnsureSuccessStatusCode();
        string responseBody = await response.Content.ReadAsStringAsync();

        return responseBody;
    }
}
```

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/456951a9-3b6b-4509-89b4-c4fe189439b2)

YO creo si quieres ver mas de esto investiga no le veo caso quiza nunca lo uses.

## File I/O

File Input/Output (I/O) is a critical aspect of many applications and is well supported in C# through the System.IO namespace. This namespace provides numerous classes that enable reading from and writing to files, creating new files and directories, and performing operations such as moving, copying, or deleting files.

The FileStream class, part of the System.IO namespace, provides a powerful and flexible interface for reading from and writing to files. As a core component of C#'s I/O library, FileStream supports both sequential and random file access, allowing you to interact with a file's content anywhere, not just at its beginning or end.

```
FileStream fs = new FileStream("test.dat", FileMode.OpenOrCreate, FileAccess.ReadWrite);

```

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/861f9b5a-ebcd-4b35-a6cc-e27358841514)


Este medoto es bastante engorroso mejro mria el siguiente

## StreamReader and StreamWriter

StreamReader and StreamWriter are powerful classes within the System.IO namespace for reading and writing character data. As high-level abstractions, they provide a more convenient interface for dealing with text files than the FileStream class.

```
        StreamWriter sw = new StreamWriter("test.txt");
        sw.WriteLine("Hello, World!");
        sw.WriteLine("Hello, World!2");
        sw.Close();

        using (StreamReader sr = new StreamReader("masa.txt"))
        {
            string line;
            while ((line = sr.ReadLine()) != null)
            {
                Console.WriteLine(line);
                Thread.Sleep(1000);
            }
        }
```

### File and Directory

Pero exite otro metodo para hacer esto 

```
File.WriteAllText("test.txt", "Hello, World!4");
```

The File and Directory classes in the System.IO namespace contain static methods for creating, copying, deleting, moving, and opening files and directories and performing various other file and directory operations.

```
        if (File.Exists("test.txt"))
        {
            Console.WriteLine("The file exists.");
        }

        File.WriteAllText("test.txt", "Hello, World! 69");
        string content = File.ReadAllText("test.txt");
        Console.WriteLine(content);
```

## Directory

The Directory class provides static methods for manipulating directories.

```
Directory.CreateDirectory("TestDirectory");
```

This code creates a new directory named TestDirectory. If the directory already exists, this method does not create a new directory but doesn’t return an error.

### Getting Files and Subdirectories

```
string[] files = Directory.GetFiles("TestDirectory");
string[] subdirectories = Directory.GetDirectories("TestDirectory");
```

## Network I/O

Network Input/Output (I/O) forms the backbone of most modern applications. It's how applications interact with networks, allowing them to send and receive data to and from remote servers.

C# provides comprehensive support for Network I/O operations through its System.Net and System.Net.Sockets namespaces, among others. These namespaces include a variety of classes and methods that encapsulate the complexity of network programming, making it easier for developers to create network-centric applications.


### HttpClient

The HttpClient class in C# is a part of the System.Net.Http namespace and provides a modern, flexible, and highly configurable way to send HTTP requests and receive HTTP responses from a resource identified by a URI (Uniform Resource Identifier). It's frequently used to consume APIs, download files, or scrape web content.

![image](https://github.com/gecr07/C-HTB-Academy/assets/63270579/3f5d1343-415b-4417-8b15-1e7b996a8cd3)

```
HttpClient client = new HttpClient();

// Send a GET request
var response = await client.GetAsync("https://api.example.com/data");

// Ensure we get a successful response
response.EnsureSuccessStatusCode();

// Read the response content
string content = await response.Content.ReadAsStringAsync();
```
Un ejemplo completo:

```
using System;
using System.Net.Http;
using System.Threading.Tasks;

class Program
{
    static readonly HttpClient client = new HttpClient();

    static async Task Main()
    {
        try
        {
            HttpResponseMessage response = await client.GetAsync("http://api.example.com/data");
            response.EnsureSuccessStatusCode();
            string responseBody = await response.Content.ReadAsStringAsync();
            Console.WriteLine(responseBody);
        }
        catch(HttpRequestException e)
        {
            Console.WriteLine("Exception Caught!");
            Console.WriteLine($"Message: {e.Message}");
        }
    }
}
```

El skill assessment te da una wordlist y tienes que hacerle fuzzing a una URL se programam


```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;
using Assessment;

class Program
{
    static readonly HttpClient client = new HttpClient();
    
    static async Task Main()
    {

        Words var = new Words();
        HashSet<string> namesHashSet = var.GetWordList();

        foreach (string name in namesHashSet)
        {
            //Console.WriteLine(name);
            try
            {
                string url = "http://10.129.205.211/";
                string url2 = name;
                string url3 = url + url2 + "/flag.txt";
                Console.WriteLine(url3);
                HttpResponseMessage response = await client.GetAsync(url3);
                response.EnsureSuccessStatusCode();
                string responseBody = await response.Content.ReadAsStringAsync();
                Console.WriteLine(responseBody);
                Console.WriteLine(name + "---------------------------");

            }
            catch (HttpRequestException e)
            {
                Console.WriteLine("Exception Caught!");
                Console.WriteLine($"Message: {e.Message}");
            }

        }

    }
}

```



