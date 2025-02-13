# SENAC Curso Desenvolvimento de Aplicativos Móveis
Usando **DART** e **FLUTTER**

------------------------------------------------------------------------------------------------------------------------

# Temas das aulas e exercícios. #

## Aula 1 - Váriaveis

### Tipos de variáveis
- **String** - textos
- **int** - números inteiros
- **double** - numeros decimais

### Práticas

**1)**
```dart
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
```dart
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
```dart
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
```dart

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

### Exemplos simples de números pares

1)
```dart
import 'dart:math' as math;
void main(){
	int conta;
  conta = 10% 2;
  print("Resultado = $conta");
}
```

2)
```
import 'dart:math' as math;
void main(){
	int numero = 666;
  if(numero % 2 == 0)
  {
    print("Par");
  }else{
    print("Ímpar");
    }
}
```

## Aula 4
//Operadores Lógicos E e OU

### Tipos de operadores lógicos
- **E** (&&) : só será verdadeiro, se todas as expressões forem verdadeiras
- **OU** (||) : só será falso, se todas as expressões forem falsas

### Teste, exercício booleano
```dart
void main(){
  bool var_a, var_b;
  
  var_a = true;
  var_b = false;
  
  print((!var_a && var_a) || (var_b || !var_b));
  
  int numero = 10;
  
  if(var_a == !var_b)
  {
  	numero = 666;  
  }
  else
  {
	numero = numero + 1;
  }
  print(numero);
}
```


## Aula 5 - Funções

### Como criar funções
- Primeiro, colocamos o RETORNO da função(tipo)
- Depois, colocamos o NOME da função
- Depois do nome, colocamos os parenteses, dentro deles, podemos colocar PARÂMETROS
- Por último, colocamos a abertura e fechamento de chaves, dentro delas irá ter o código da função. 
- IMPORTANTE: Devemos chamá-las após todo esse processo!

```dart
void main() {
 print("Minha calculadora");
  
  double n1, n2;
    n1 = 10;
  	n2 = 5;
  
  calcular(n1,n2,"+");
  calcular(n1,n2,"-");
  calcular(n1,n2,"*");
  calcular(n1,n2,"/");
}

/*Como cria uma função?
 * 
 * Primeiro, colocamos o RETORNO da função(tipo)
 * Depois, colocamnos o NOME da função
 * Depois do nome, colocamos os parenteses, dentro deles, podemos colocar PARÂMETROS
 * Por último, colocamos a abertura e fechamento de chaves, dentro delas irá ter o código da função.
 * 
 * IMPORTANTE: Só criar a função não serve pra NADA. A gente te, que CHAMAR essa função no main
*/

void calcular(double novoNumero1, double novoNumero2, String operacao){
	print("\nQuanto é $novoNumero1 $operacao $novoNumero2?");
  double resposta;
  
  if(operacao == "+"){
    resposta = novoNumero1 + novoNumero2;
  }else if(operacao == "-"){
    resposta = novoNumero1 - novoNumero2;
  }else if(operacao == "/"){
    resposta = novoNumero1 / novoNumero2;
  }else if(operacao == "*"){
    resposta = novoNumero1 * novoNumero2;
  }else{
    resposta = 0;
  }
  
  print("O resultado é: $resposta");
}
```

## Aula 6 - Flutter
Entramos em flutter,dev (ou flutter.io) e prcuramos o local pra começar a utilizar o flutter (Get Started). Seguimos os seguintes passos:
- Baixar o SDK do flitter e colocamos na pasta "C:/src/flutter"
- Baixar e instalar o Android Studio
- Configurar o plugin do flutter no Android Studio
- Rodar o comando "flutter doctor" no Prompt de Comando para certificar que está tudo ok.

### Criação do primeiro App
**IMPORTANTE: Nunca feche a máquina virtual**

1. Abrir o Android Studio
2. Abrir a Máquina Virtual (emulador do Android)
3. Apertar o botão "Start new Flutter Project" (iniciar novo projeto do flutter)
4. Escolher aplicativo flutter
5. Colocar nome, descrição, e o caminho do SDK
6. Nome da empresa (não mudou nada)

### Analisando código pronto do Android Studio
- Sintaxe é um modo como você faz algo corretamente
-- O *primarySwatch: Colors.purple* nos deixa alterar a cor tema do aplicativo (barra do menu e botão)
-- *MyHomePage(title: 'Meu Primeiro Aplicativo'* é o nome que aparecerá na barra fixa do aplicativo) e é uma classe para alterar as coisas na tela
-- *MuHomePageState*
- O Flutter Inspector nos mostra o código de forma gráfica
- Widgets são ferramentas (flutter nos dá para construir nosso app)


```dart
import 'package:flutter/material.dart';
//O *import* importa um pacote de material do dart para podermos usar

void main() => runApp(MyApp());
//O *void main* é uma função que chama outra, a *runApp* (função que roda o app). O runApp chama a classe *myApp*

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        // This is the theme of your application.
        //
        // Try running your application with "flutter run". You'll see the
        // application has a blue toolbar. Then, without quitting the app, try
        // changing the primarySwatch below to Colors.green and then invoke
        // "hot reload" (press "r" in the console where you ran "flutter run",
        // or simply save your changes to "hot reload" in a Flutter IDE).
        // Notice that the counter didn't reset back to zero; the application
        // is not restarted.
        primarySwatch: Colors.purple
      ),
      home: MyHomePage(title: 'Meu Primeiro Aplicativo'),
    );
  }
}

class MyHomePage extends StatefulWidget {
  MyHomePage({Key key, this.title}) : super(key: key);

  // This widget is the home page of your application. It is stateful, meaning
  // that it has a State object (defined below) that contains fields that affect
  // how it looks.

  // This class is the configuration for the state. It holds the values (in this
  // case the title) provided by the parent (in this case the App widget) and
  // used by the build method of the State. Fields in a Widget subclass are
  // always marked "final".

  final String title;

  @override
  _MyHomePageState createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  int _counter = 0;

  void _incrementCounter() {
    setState(() {
      // This call to setState tells the Flutter framework that something has
      // changed in this State, which causes it to rerun the build method below
      // so that the display can reflect the updated values. If we changed
      // _counter without calling setState(), then the build method would not be
      // called again, and so nothing would appear to happen.
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    // This method is rerun every time setState is called, for instance as done
    // by the _incrementCounter method above.
    //
    // The Flutter framework has been optimized to make rerunning build methods
    // fast, so that you can just rebuild anything that needs updating rather
    // than having to individually change instances of widgets.
    
    return Scaffold(
    // O Scaffold é quem constroe a página pra gente
      appBar: AppBar(
        // Here we take the value from the MyHomePage object that was created by
        // the App.build method, and use it to set our appbar title.
        title: Text(widget.title),
      ),
      body: Center(
        // Center is a layout widget. It takes a single child and positions it
        // in the middle of the parent.
        child: Column(
          // Column is also layout widget. It takes a list of children and
          // arranges them vertically. By default, it sizes itself to fit its
          // children horizontally, and tries to be as tall as its parent.
          //
          // Invoke "debug painting" (press "p" in the console, choose the
          // "Toggle Debug Paint" action from the Flutter Inspector in Android
          // Studio, or the "Toggle Debug Paint" command in Visual Studio Code)
          // to see the wireframe for each widget.
          //
          // Column has various properties to control how it sizes itself and
          // how it positions its children. Here we use mainAxisAlignment to
          // center the children vertically; the main axis here is the vertical
          // axis because Columns are vertical (the cross axis would be
          // horizontal).
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'You have pushed the button this many times:',
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.display1,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
}

```


### Estrutura básica de todo aplicativo

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MeuApp());
}

class MeuApp extends StatefulWidget{
  @override
  State<StatefulWidget> createState( {
    //TODO: implement createState
    return _MeuAppState();
  })
}

class MeuAppState extends State<MeuApp>{
  @override
  Widget build(BuildContext context) {
    // TODO: implement build
    return null;
  }
  
}
```

## Aula 7 - 

### Estrutura em que trabalhamos algumas propriedades
```dart
import 'package:flutter/material.dart';

void main() {
  runApp(
      new Material(
        color: Colors.lightBlue,
        child: new Center(
          child: new Text("Hello World", textDirection: TextDirection.ltr,
          style: new TextStyle(fontSize: 40, color: Colors.black
            ),
          ),
      )
    )
  ) // runApp
} //void main
```
