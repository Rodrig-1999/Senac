# SENAC
Curso Desenvolvimento de Aplicativos Móveis
Usando **DART** e **FLUTTER**

## Aula 1 - Váriaveis

### Tipos de variáveis
- **String** - textos
- **int** - números inteiros
- **double** - numeros decimais

------------------------------------------------------------------------------------------------------------------------

### Práticas

**1)**
```
//Colocamos pra imprimir na tela algumas coisinhas e criamos algumas variáveis basicas,
devemos lembrar que quando não colocamos o tipo de variavel,
ela é configurada para ser sempre o que teve depois do igual

// main = principal
/* Variavel: Um valor (número, texto, valor lógico, etc)
armazenado na memória ram do computador,que perde seu valor
sempre que o PC é desligado. Seu valor pode ser modificado a qualquer momento. */

void main() {
  print("Olá World");
  print("Olá Rodrigo");
  
  var nome = "Juliet"; //Como não foi especificado o "String", a variavel já "salva" que ela deve ser sempre texto
  var numero = "1";
  print("Bom dia, " + nome);
  
  print ("Numero: $numero");
  
}
```
------------------------------------------------------------

**2)**
```
//Cálculo simples com casas decimais

void main() {
 var sorteio = 5;
  sorteio = 5 - 1;
  sorteio = sorteio * 2;
  print (sorteio);
  
 //String = texto
 String nome, sobrenome;
  nome = "Oliver";
  sobrenome = "Queen";
  print("Hello, $nome $sobrenome");
  
 //double = números decimais (com casas)
  double altura, peso, imc;
  altura = 1.60;
  peso = 53;
  imc = peso / (altura * altura);
  print ("Seu imc é $imc");
}
```
------------------------------------------------------------

**3)**
```
//Criar variaveis pelo nome, sobrenome, email e ano de nascimento. Calcular a idade e mostrar ao final
uma mensagem com todos esses dados.

void main() {
  String nome, sobrenome, email;
  nome = "Rodrigo";
  sobrenome = "Santos";
  email = "rodrigo.santoss23sv@gmail.com";
      
  int anonascimento, anoatual, idade;
  anonascimento = 2002;
 	idade = 2019 - anonascimento;
 
  print('Olá, $nome $sobrenome,\no e-mail fornecido por você foi "$email".\nVocê tem $idade anos.');
}
```

## Aula 2

**${renda_pessoa.toStringAsFixed(2)}**

O método toStringAsFixed() foi usado para formatar as casas (2) decimais da variável(renda_pessoa) double.

```dart
void main() {
  String nome, sobrenome, email, senha, cpf, endereco, sexo, celular, curso, nome_social;
  int ano_nasc, idade, qtd_moradores;
  double renda_familiar, renda_pessoa;
 

  nome = "Thiago Antonio" ;
  sobrenome = "dos Santos Oliveira";
  nome_social = "";
  email = "braddock@hotmail.com";
  senha = "123changeja" ;
  cpf = "111.222.333-66";
  endereco = "Rua dos Alfeneiros 9.3/4";
  sexo = "masculino";
  celular = "(19)99666-0000";
  curso = "Programador de Disp. Móveis";
  ano_nasc = 1989;
  idade = 2019 - ano_nasc;
  qtd_moradores = 2;
  renda_familiar = 5355.22;
  renda_pessoa = renda_familiar / qtd_moradores;

  print("**************************");
  print("Confirmação de Cadastro");
  print("**************************");
  print("\nNome: $nome $sobrenome");

  if (nome_social != "")
  {
    print("Nome Social: $nome_social");
  }

  print("E-mail: $email");
  print("Sexo: $sexo");
  print("Celular: $celular");
  print("Ano de Nascimento: $ano_nasc");
  print("Idade: $idade");
  print("CPF: $cpf");
  print("\n**************************");
  print("Informações SENAC");
  print("**************************");
  print("\nCurso: $curso");
  print("Endereço: $endereco");
  print("Moradores na mesma residência: $qtd_moradores");
  print("Renda Familiar: R\$ $renda_familiar");
  print("Renda por pessoa: R\$ ${renda_pessoa.toStringAsFixed(2)}");
 
}

```

### Condição Lógica IF

O IF serve para determinar se um bloco de instruções **deve** ou **não** ser executado, pode-se dizer que sempre que for necessário **testar** algum valor usaremos o *if*.

### Operadores Lógicos

- == *Igualdade*
- != *Diferente*
- \>= *Maior ou igual* 
- <= *Menor ou igual*
- \>  *Maior*
- <  *Menor*

### Sintaxe

```dart
if(teste_logico)
{
    //faz isso se o teste for verdadeiro
}
else
{
    //faz isso se o teste for falso
}
```

### Exemplo if :floppy_disk:
```dart
string curso = "programador android";

if(curso == "programador android")
{
    print("Parabéns, você faz ótimas escolhas.");
}
else
{
    print("Vacilão, aposto que você faz ADM.");
}
```
### Exemplo if 2

```dart
void main() {
	double nota1, nota2, media;
  nota1 = 5;
  nota2 = 2;
  media = (nota1 + nota2) / 2;
  if(media >= 5)
  {
  		print("Aprovado com média $media");
  }
  else
  {
    	print("Reprovado com média $media");
  }
}
```

## Aula 3

// Foi importada a *biblioteca* **darth:math** para podermos usar funções matemáticas como potência e raiz quadrada, no exemplo abaixo foi usada a função **math.sqrt()** para calcular a raiz de delta.
- Após a importação foi dado um apelido para chamar a função através da sintaxe **as** (dart:matg as **math**)
- Foram usados 2 ifs, o primeiro para dar acesso através da palavra mágica STRANGER e o segundo para fazer a equação.
- Cada if tem seu própio else, daí a importância de *identar*, organizar o código com **TABS**

### Exemplos usando math
```dart
print(math.sqrt(9)); //exibe a raiz de 9
print(math.pi); //exibe o valor de pi
print(math.pow(2,7)); //exibe o resutado de 2 elevado a 7
```

### Exemplos usando if dentro de if (if aninhado ou encadeado)

Quando temos mais do que 2 testes possíveis, é necessário alterar a estrutura e acrescentar um **else if** após o primeiro if

1)
```dart
import 'dart:math' as math;
void main() {
  String palavra_magica;
  palavra_magica = "stranger";
  
  if(palavra_magica == "stranger"){
    print("Exercício 1 - Bhaskara");
    
    double delta, a, b, c, x;
    a = 1;
    b = -10;
    c = 25;
    delta = (b * b)- 4 * a *c;
    
    print("Delta = $delta");
    
    if(delta < 0){
      
    	print("Não há nenhuma raíz real, pois o Delta é menor que zero");
    }
    else{
      
    	double raiz_q, x1, x2;
    //Raiz quadrada
      raiz_q = math.sqrt(delta);	//para a operação de raiz quadrada
      x1 = (-b + raiz_q) / (2 * a);
      x2 = (-b - raiz_q) / (2 * a);
      
      print("Raiz do Delta = $raiz_q");
      print("X1 = $x1");
      print("X2 = $x2");
      print("Houve uma raíz real, pois o delta é maior que zero");
    }
    
    }else{
      print("Acesso negado!");
    }

}
```

2)
```
// toLowerCase compara a coisa digitada com a fixa, tudo em minúsculo

void main(){
 String cidade_natal;
 cidade_natal = "São João da Boa Vista";
  
if(cidade_natal.toLowerCase() == "são joão da boa vista")
{
 print("São joanense");
 
}else if(cidade_natal.toLowerCase() == "jundiai"){
print("Jundiaiense");

}else if(cidade_natal.toLowerCase() == "campos do jordão"){
print("Jordanense");

}else if(cidade_natal.toLowerCase() == "ribeirão-preto"){
print("Ribeirão-pretano");

}else if(cidade_natal.toLowerCase() == "franco"){
print("Francano");

}else if(cidade_natal.toLowerCase() == "santa isabel"){
print("Isabelense");

}else{
print("Cidade não cadastrada, infelizmente só registramos cidades do estado de São Paulo. Adicionaremos o mais rápido possível.");
}

}
```

