# Primeiro-reposit-rio---Aprendendo-automação-de-testes
Utilizando selenium

using OpenQA.Selenium;
using OpenQA.Selenium.Chrome;
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {

            Console.WriteLine("Hello World!");
            IWebDriver driver = new ChromeDriver();
            driver.Navigate().GoToUrl("https://iterasys.com.br/login/");
            driver.Manage().Timeouts().ImplicitWait = TimeSpan.FromSeconds(5);
            //driver.FindElement(By.CssSelector("//a[@href='https://www.globo.com']")).Click();
            IWebElement campologin = driver.FindElement(By.Id("email"));
            campologin.SendKeys("claudiasousa683@gmail.com");
            IWebElement camposenha = driver.FindElement(By.Id("senha"));
            camposenha.SendKeys("24061512");
            IWebElement botao = driver.FindElement(By.Id("btn_login"));
            botao.Click();


        }
    }

}

