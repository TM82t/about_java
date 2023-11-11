# Java
## Javaは現在最も広く使われている言語の1つ。多くのソフトウェアエンジニアがJavaを駆使し、開発を進めている。  
## このリポジトリにはJavaの基本的なことをアウトプットしていく。
### Javaの基本・文字列
#### Javaの場合も文字列はダブルクォーテーション（"）で囲む必要がある。" "で囲んでいないと、コードが動かなくなる。
* 文字列の例：System.out.println("Hello World"); → 「()の中身(Hello World)を出力（表示）せよ」という「命令」
#### Javaの構造はクラス部分、メソッド部分、処理部分の3つに分けられる。
* クラスの中にメッソド、メッソドの中に処理部分が存在している。
#### Javaでは文の終わりにセミコロン（;）を付けなければならず、忘れるとコードが動かなくなる。
#### Javaのコード内にコメントを書く時は文の頭に「//」と書く。そうすることでそこから行末までがコメントとみなされる。
### 数値
#### Javaも数値は文字列と違い、ダブルクォーテーションで囲まない。例は以下の通り。
* System.out.println(5); → 出力結果 : 5
* System.out.println(5 + 2); → 出力結果 : 7
#### 仮にダブルクォーテーションで囲んだ場合は文字列判定となり、以下の通りに出力される。
* System.out.println("5 + 2 "); → 出力結果 : 5 + 2
#### 足し算以外にも引き算、掛け算、割り算の出力が可能。例は以下の通り。
* System.out.println(5 - 2); → 出力結果 : 3
* System.out.println(5 * 2); → 出力結果 : 10
* System.out.println(6 / 2); → 出力結果 : 2
* System.out.println(5 % 2); → 出力結果 : 1(計算結果は2余り1、余りが出たら余り部分が出力される)
