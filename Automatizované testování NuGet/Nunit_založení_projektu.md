

dotnet add package Selenium.WebDriver

Nunit3TestAdapter


**Nainstalovat do PC:**

.NET 7.0 nebo 6.0 s dlouhou podporou

Visual Studio Code

nebo 

Visual Studio 2022 - pouze WIN a MacOS


**Potřebná rozšíření:**

.NET Extension Pack

C#

Nuget Package Manager



**Postup vs code:**


dotnet new nunit 

dotnet new nunit -n MyNUnitProject  ---> vytvoří novou složku s projektem název je možno upravit


dotnet add package Nunit3TestAdapter  ---> nutné také stáhnout

dotnet add package NUnit.ConsoleRunner --> GitHub Actions

dotnet add package Selenium.WebDriver - stahne knihovny selenium přejít do složky projektu

Tento návod funguje jak pod Linux (odzkoušené v distribucích EndeavorOS, Ubuntu 22.04), MacOS, Windows 11.

Z důvodu kompaktibility jseou je na GitHub pouze samotný kód testu. Ostatní soubory a složky se vytvoří po založení projektu.

Složka TestResults také není součásti verze GitHub.

.....................................................................................................................................

aby test prošel je potřeba zkontrolovat hlavičku testu:

using OpenQA.Selenium;
using OpenQA.Selenium.Chrome;
using System;
using NUnit.Framework;
using System.Threading;
