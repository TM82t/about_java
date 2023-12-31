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
#### 型・・・変数に予期しない種類の情報が入ってしまうことを未然に防ぐための安全装置の役割を果たしている。
#### 型によって担保される安全性を「型安全（type safe）」という。
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
  
#### String型変数の連結・・・文字列の入った変数であれば、文字列と同様に連結を行うことが可能。
####                    なお、変数にダブルクォーテーションを付けると、変数ではなく文字列として扱われてしまう。
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
number += 3; // 変数に3を足す
number -= 3; // 変数から3を引く
number *= 3; // 変数に3を掛ける
number /= 3; // 変数を3で割る
number %= 3; // 変数を3で割る（小数点も表示)
// 変数に1を足す、もしくは1を引く場合はさらに省略可能
number++; // 変数に1を足す
number--; // 変数に1を引く
```
#### 変数の注意点・・・変数名は基本的に自由に決めらるが、Javaでは何個か決まりがある。
良い例・・・問題なく処理されるパターン  

|例|理由|
|:---|:---|
|date|英単語を用いる|
|userName|2語以上の変数名を使うときは、単語の始めを大文字にして区切る。この記述法をキャメルケースと呼ぶ。|  

悪い例・・・エラーが発生するパターン  
  
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
#### キャスト・・・強制型変換を用いた整数と小数点の計算
```
int x = 13;
int y = 4;
System.out.println(x / y); // 結果：3（3.25とは出ない）

System.out.println((double)x / y); // 結果：3.25
```
強制的に型変換を行うことをキャストと呼び、(変換したいデータ型)値とする。  
int型同士の値から、最終的にdouble型の計算結果を得たい場合、どちらか1つをキャストする。  
片方がdouble型であれば結果はdouble型になる。  

### if文
int time = で定義する数値で結果が変わるよう else if を用いて記述。
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
  
### 真偽値
真偽値のデータ型はboolean型。  
true, falseにはダブルクォーテーションは付けないことに注意。  
ダブルクォーテーションを付けるとString型(文字列)になる。  
```
System.out.println(true); // 出力結果：true
System.out.println(false); // 出力結果：false
```
  
### 比較演算子
値を比較するための記号で、比較した結果は真偽値（trueかfalse）になる。  
「x == y」はxとyが同じかどうかを比較し、同じであればtrue、  
違っていればfalseとなる。また「x != y」はその逆になる。  
代入の「=」と比較の「==」を混同しないように注意。  
並びに以上及び以下はそれぞれ「<=」「>=」で比較可能。
```
System.out.println(5 + 2 == 7); // 出力結果：true
System.out.println(5 + 2 == 6); // 出力結果：false
System.out.println(5 + 2 != 7); // 出力結果：false
System.out.println(5 + 2 != 6); // 出力結果：true

System.out.println(5 + 2 >= 7); // 出力結果：true
System.out.println(5 + 2 >= 8); // 出力結果：false
System.out.println(5 + 2 >= 8); // 出力結果：false
System.out.println(5 + 2 >= 6); // 出力結果：true
```
### 比較演算子
論理演算子は「かつ」「または」「~でない」を表現する記号。  
「かつ」は&&で表現し、「条件1 && 条件2」は「条件1がtrueかつ条件2もtrue」  
ならば結果もtrueになり、どちらか一方でもfalseならば結果はfalseになる。  
  
「または」は||で表現し、「条件1 || 条件2」は、  
「条件1または条件2のどちらか一方でもtrue」であれば結果はtrueになる。  
  
!を用いると「〜でない」を表現できる。例えば、!(x >= 30)は  
「xが30以上でない（30より小さい）」ときtrueになり、「xが30以上」のときfalseになる。  

### switch文
switch文は下図のように記述し、条件の値がcaseの値と一致するとき、処理が実行される。
switch文は構文が少し複雑。caseの後ろのコロン（:）などは忘れがちなので注意。  
breakはswitch文を終了する命令であり、非常に重要。  
breakがないと、合致したcaseの処理を行った後、その次のcaseの処理も実行してしまう。  
意図せぬ処理が起こるため、switch文を使うときはbreakを忘れないよう気をつける。  
```
int n = 1
switch (n) {
 case 1:
  System.out.println("大吉");
  break;
 case 2:
  System.out.println("吉");
  break;
}
```
どのcaseとも一致しなかったときに実行する処理を、defaultに指定することが可能。if文のelseに似ている。  
  
### whileによるループ処理
次のコードは i に変数の初期値を代入し、i が定めた数値を上回るまで繰り返し処理を行うように記述している
```
public class Main {
    public static void main(String[] args) {
        int i = 0; // カウンタ変数の初期化
        while (i <= 8) {
            System.out.println("hello world " + i);// 繰り返し処理
            i = i + 1; // カウンタ変数を更に i++; と記述もできる
        }
        System.out.println("last " + i); // ループ処理後のiを確認
    }
}
```
出力結果  
hello world 0  
hello world 1  
hello world 2  
hello world 3  
hello world 4  
hello world 5  
hello world 6  
hello world 7  
last　8  
上の記述で最後に変数iに1を足し忘れると変数iは1のまま変わらず、条件が永遠にtrueになってしまい、繰り返し処理が無限に行われてしまう（無限ループ）。  
無限ループはコンピュータに異常な負荷をかけることになるので、確実に阻止する必要がある。繰り返し処理では、必ずどこかで条件がfalseになるように実装する。  

### for文
for文では、forの後の()内に、「変数の初期化、条件式、変数の更新」の3つを記述。  
それぞれはセミコロン（;）で区切るが、最後の変数の更新にはセミコロン（;）をつけないことに注意。  
例
```
class Main {
  public static void main(String[] args) {
    for(int i = 1; i <= 10; i++) {
      System.out.println(i + "回目のループです");
    }
    
  }
}
```
  
### break, continue
繰り返し処理を終了するためには、条件をfalseにする以外にbreakを使って強制的に終了させる方法がある。  
繰り返し処理を終了するbreakと違い、continueはその周の処理だけをスキップし、次の周を実行することができる。  
if文などと組み合わせて利用するのが一般的。
例
```
class Main {
  public static void main(String[] args) {
    System.out.println("=== while文 ===");
    int i = 1;
    while (i < 10) {
      // iが5の倍数のとき、繰り返し処理を終了
      if (i % 5 == 0) {
        break;
      }
      
      System.out.println(i);
      i++;
    }
    
    System.out.println("=== for文 ===");
    for (int j = 1; j < 10; j++) {
      // jが3の倍数のとき、処理をスキップ
      if (j % 3 == 0) {
        continue;
      }
      
      System.out.println(j);
    }
  }
}
```
  
### 配列
配列とは、変数のセットのようなもの。変数が1つしか値を扱えないのに対し、配列は複数の値をまとめていれておくことが可能。  
配列は仕切りのある箱のようなもので、それぞれのスペースに値が入っている。配列に入っているそれぞれの値のことを要素と呼ぶ。  
配列の要素には、前から順に「0, 1, 2・・・」と数字が割り振られている。これをインデックス番号といい、0から始まる点に注意。  
例
```
class Main {
  public static void main(String[] args) {
    // 変数namesに、配列を代入
    String[] names = {"にんじゃわんこ", "ひつじ仙人", "ベイビーわんこ"};
    
    // インデックス番号が0の要素を出力
    System.out.println(names[0]);
    
    // インデックス番号が2の要素を出力
    System.out.println(names[2]);
    
  }
}
```
### 配列の上書き
配列の各要素は変数のようなもの。特定の要素に値を代入することで要素を上書きすることが可能。  
配列では存在しない要素に値を代入することはできないので注意。  
例
```
class Main {
  public static void main(String[] args) {
    String[] languages = {"Ruby", "PHP", "Python"};

    System.out.println(languages[1]);
    
    languages[1] = "Java";
    
    System.out.println(languages[1]);
    
  }
}
```
出力結果  
PHP  
Java  

### 配列とfor文
for文を用いることで、配列の要素の値を簡単に一覧表示できる。
```
class Main {
  public static void main(String[] args) {
    String[] names = {"John", "Kate", "Bob"};

    for(int i = 0; i < 3; i++) {
      System.out.println("Hello" + names[i]);
    }
    
  }
}
```
出力結果  
Hello John  
Hello Kate  
Hello Bob

### length
配列には要素の数を数えるlengthという機能が備わっている。lengthは「配列.length」のようにドット（.）でつないで用いる。  
lengthを用いれば、上記のfor文の条件式「i < 3」を下記のように書き換えることができ、配列の要素数を気にする必要がなくなる。  
```
class Main {
  public static void main(String[] args) {
    String[] names = {"John", "Kate", "Bob"};

    for(int i = 0; i < names.length; i++) {
      System.out.println("Hello" + names[i]);
    }
    
  }
}
```
  
### 拡張for文の文法
for文は配列用に特別な構文（拡張for文）を用意している。これを使えば、for文をよりシンプルに書くことが可能。  
```
class Main {
  public static void main(String[] args) {
    String[] names = {"わんこ", "ひつじ", "ねこ"};
    
    for (String name: names) {
      // データ型 変数名 配列名
      System.out.println("私の名前は" + name + "です");
    }
    
  }
}
```
出力結果  
私の名前はわんこです  
私の名前はひつじです  
私の名前はねこです
