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






















































