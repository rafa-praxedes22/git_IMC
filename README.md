# git_IMC
Incluir linha

adicionar linha
import java.util.Scanner;

public class Calculoimc {

    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        String nome1, nome2;
        float peso1, peso2, altura1, altura2;
        float imc1, imc2;
        String classifica1, classifica2;
        System.out.println("Nome da Pessoa 1: ");
        nome1 = ler.nextLine();
      System.out.println("Peso da Pessoa 1 (kg): ");
      peso1 = ler.nextFloat();
      System.out.println("Altura da Pessoa 1 (m): ");
      altura1 = ler.nextFloat();
      ler.nextLine();
 
      System.out.println("Nome da Pessoa 2: ");
      nome2 = ler.nextLine();
      System.out.println("Peso da Pessoa 2 (kg): ");
      peso2 = ler.nextFloat();
      System.out.println("Altura da Pessoa 2 (m): ");
      altura2 = ler.nextFloat(); 
      ler.nextLine();
 
      imc1 = calcularIMC(peso1,altura1);
      imc2 = calcularIMC(peso2,altura2);
 
      classifica1 = resultadoIMC(imc1);
      classifica2 = resultadoIMC(imc2);
 
      System.out.printf("IMC da Pessoa 1 = %.1f - %s\n",imc1,classifica1);
      System.out.printf("IMC da Pessoa 2 = %.1f - %s\n\n",imc2,classifica2);
 
      if (imc1 > imc2)
      {
         System.out.println("A Pessoa \""+nome1+"\" tem Maior IMC");
      }
      else
      {
         System.out.println("A Pessoa \""+nome2+"\" tem Maior IMC");
      }
 
      //System.out.println("A Pessoa \""+(imc1 > imc2 ? nome1 : nome2)+"\" tem Maior IMC");

   } 
 
   static float calcularIMC(float p, float h)
   {
      return p/(h*h);
   }


   static String resultadoIMC(float imc)
   {
      String result;
      if (imc <= 19)
         result = "Abaixo do Peso";
      else
         if (imc <= 25)
            result = "Peso ideal";
         else
            if (imc <= 30)
               result = "Acima do Peso";
            else
               if (imc <= 35)
                  result = "Obesidade Leve";
               else
                  result = "Obesidade"; 
      
      return result;

    }
}