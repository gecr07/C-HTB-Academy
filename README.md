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
















