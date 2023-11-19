# Java
## Javaは現在最も広く使われている言語の1つ。多くのソフトウェアエンジニアがJavaを駆使し、開発を進めている。  
## このリポジトリにはJavaの基本的なことをアウトプットしていく。
### Javaが人気の理由
#### Javaの最大の特徴は、「一度プログラムを書けばどこでも動く」と言う点。
#### Javaは一度プログラムを書けば、違う種類のコンピュータでもどこでも動く。
### Javaの基本・文字列
#### Javaの場合もRuby同様、文字列はダブルクォーテーション（"）で囲む必要がある。" "で囲んでいないと、コードが動かなくなる。
* 文字列の例：
```
class Main {
  public static void main(String[] args) {

    System.out.println("Hello World");

 }
}
```
「()の中身(Hello World)を出力（表示）せよ」という「命令」
#### Javaは実行前にコードをコンピュータ用に変換する「コンパイル」を行う。
#### Javaの構造はクラス部分、メソッド部分、処理部分の3つに分けられる。
* クラスの中にメッソド、メッソドの中に処理部分が存在している。
#### Javaのmainメソッドとは、必ずはじめに実行されるJavaプログラムのメソッドのこと。
* プログラムにmainメソッドがない場合、プログラムを実行すると次のようなエラーが返される。
```
java.lang.NoSuchMethodError: main
Exception in thread "main"
```
#### Javaプログラムではmainメソッドがプログラムの入り口となって実行されるため、mainメソッドを正しく準備しておく必要がある。
#### Javaでは文の終わりにセミコロン（;）を付けなければならず、忘れるとコードが動かなくなる。
#### Javaのコード内にコメントを書く時は文の頭に「//」と書く。そうすることでそこから行末までがコメントとみなされる。　　
　　
### 数値
#### Javaも数値は文字列と違い、ダブルクォーテーションで囲まない。例は以下の通り。
例1
```
System.out.println(5);
```
出力結果 : 5  
例2
```
System.out.println(5 + 2);
```
出力結果 : 7
  
#### 仮にダブルクォーテーションで囲んだ場合は文字列判定となり、以下の通りに出力される。
```
System.out.println("5 + 2 ");
```
出力結果 : 5 + 2
#### 足し算以外にも引き算、掛け算、割り算の出力が可能。例は以下の通り。
例1
```
* System.out.println(5 - 2);
```
出力結果 : 3  
例2
```
System.out.println(5 * 2);
```
出力結果 : 10  
例3
```
System.out.println(6 / 2);
```
出力結果 : 2  
例4
```
System.out.println(5 % 2);
```
出力結果 : 1(計算結果は2余り1。「%」は余りを計算でき、出たら余り部分が出力される)　　
    
### 文字列の連結
#### Rubyと同様に文字列を「足し算」すると、下記のように文字列を連結することが可能。
例1
```
System.out.println("Hello" + "World");
```
出力結果 : HelloWorld  
例2
```
System.out.println("5" + "2");
```
出力結果 : 52　　
  
### 変数の定義
#### データ型　文字列 → String型、整数　→ int型
#### 変数の値の代入は変数定義と同時に行うことができる。変数定義と同時に値を代入することを変数の初期化と呼ぶ。
例1
```
int number = 3;
```
例2
```
String text = "Hello World";
```
#### int型変数の計算・・・数値が入った変数なら、数値と同様に計算が可能。数値と変数の計算も、変数同士の計算もできる。例は以下の通り。
例1
```
int number1 = 10;
System.out.println(number1 + 3);
```
出力結果 : 13  
例2
```
int number1 = 10;
int number2 = 5;
System.out.println(number1 + number2);
```
出力結果 : 15  
  
#### String型変数の連結・・・文字列の入った変数であれば、文字列と同様に連結を行うことが可能。なお、変数にダブルクォーテーションを付けると、変数ではなく文字列として扱われてしまう。
```
String greeting = "こんにちは";
System.out.println(greeting + "佐藤さん");
```
出力結果　： こんにちは佐藤さん

#### 変数の更新・・・一度値を代入した変数にその後再び値を代入すると、後で代入した値によって変数の中身が上書きされる。  
例
```
String name = "Sato";
System.out.println(name);

name = "Suzuki";
System.out.println(name);
```
出力結果  
Sato  
Suzuki
値を更新する際、データ型を変数名の前に記述しないこと。同じ処理内で同一名の変数を定義できないため、エラーとなる。  
  
#### 自己代入・・・例として変数numberに2が入っており、3を足して上書きしたい場合等に使う。  
この時、代入の「=」は等しいわけではないことがポイント。
```
int number = 2;
System.out.println(number); // 出力結果 ： 2
x = number + 3;
System.out.println(number); // 出力結果 : 5
```
#### 自己代入の省略した記述
```
int number = 2;
number += 3;
number -= 3;
number *= 3;
number /= 3;
number %= 3;
// 変数に1を足す、もしくは1を引く場合はさらに省略可能
number++; // 変数に1を足す
number--; // 変数に1を引く
```
#### 変数の注意点・・・変数名は基本的に自由に決めらるが、Javaでは何個か決まりがある。
良い例  

|例|理由|
|:---|:---|
|date|英単語を用いる|
|userName|2語以上の変数名を使うときは、単語の始めを大文字にして区切る。この記述法をキャメルケースと呼ぶ。|  

悪い例  
  
|例|理由|
|:---|:---|
|1name|数字開始。エラーが出る。|
|first_name|アンダーバー（スネークケース）は望ましくない。|
|namae|ローマ字も紛らわしく、分かりにくため望ましくない。|
|名前|日本語もプログラミングでは望ましくない。|
  
#### 少数点・・・少数を表すデータ型は基本的にdouble型を使用。例は以下の通り。
```
double number1 = 5.38;
double number2 = 2.34;
System.out.println(number1 + number2); // 出力結果 : 7.72
```
#### 強制型変換を用いた整数と小数点の計算
```
int x = 13;
int y = 4;
System.out.println(x / y); // 結果：3（3.25とは出ない）

System.out.println((double)x / y); // 結果：3.25
```
### if文
```
int time = 8;
if((time >= 4) && (time <= 10)){
  System.out.println("只今の時刻は" + time + "時です。");
  System.out.println("おはようございます");
}else if((time >= 11) && (time <= 17)){
  System.out.println("只今の時刻は" + time + "時です。");
  System.out.println("こんにちは");
}else if(time == 18){
  System.out.println("只今の時刻は" + time + "時です。");
  System.out.println("こんばんは");
}else if((time >= 19) && (time <= 3)){
  System.out.println("只今の時刻は" + time + "時です。");
  System.out.println("おやすみなさい");

 // 出力結果:只今の時刻は8時です。おはようございます。
```
