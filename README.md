# csharp-tarefa
using System;

namespace programa
{
    class Program
    {

        static void Cadastrar(string username, string password)
        {
            string usuarios = File.ReadAllText("cadastro.txt");
            //verificar se user ja existe

        }

        static void Main(string[] args)
        {
            Console.WriteLine("Olá");
            Console.WriteLine("Digite 1 para cadastrar.");
            Console.WriteLine("Digite 2 para logar.");
            Console.WriteLine("Digite 3 para sair.");
            bool sair = false;
            while(!sair)
            {
                var opcao = 0;
                try
                {
                opcao = int.Parse(Console.ReadLine());
                }
                catch(Exception e)
                {

                }

                switch(opcao){
                    case 1:
                    Console.WriteLine("Digite um nome de usuário");
                    string username = Console.ReadLine();
                    Console.WriteLine("Digite uma senha");
                    string password = Console.ReadLine();
                    Console.WriteLine("Confirme a senha");
                    string confirmacao = Console.ReadLine();
                    if(password != confirmacao)
                    {
                        Console.WriteLine("As senhas não conferem!");
                    }
                    else
                    {
                        Cadastrar(username, password);
                    }
                    break;
                    
                    case 2:
                    break;

                    case 3:
                    sair = true;
                    break;

                    default:
                    Console.WriteLine("Opção inválida, tente novamente!");
                    break;
                }
            }
        }
    }
}

