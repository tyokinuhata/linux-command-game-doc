# Linuxコマンドゲームとは
Linuxコマンドゲームとは, 様々なLinuxコマンドを駆使して戦う新しいカードゲームです.

ルールはいたってシンプルで, 先に自分の手札を０枚にした方が勝利です.

# 用語

|用語|説明|
|:--|:--|
|リポジトリ|山札のこと|
|ワークツリー|手札のこと|
|コミッター|プレイヤーのこと|
|コマンド|カードのこと|

# ルール
基本的に２人以上で行うゲームです.

コミッターはそれぞれリポジトリから５枚コマンドを引き, さっそくゲームスタートです.

コミッターは毎ターン１枚のコマンドをリポジトリから引き, ワークツリーに加えます.

その後, コミッターはワークツリーの中から０以上の任意のコマンドを実行します.

実行したコマンドに応じた処理を行い, 自分のターンを終了とします.

この一連の流れを繰り返し, 先に０枚になったコミッターが勝利です.

# コマンド一覧

|コマンド名|処理|
|:--|:--|
|cat|相手のワークツリーを全て見る.|
|ls|お互いのコミッターは１ターンの間, ワークツリーを開示する.|
|cp|ワークツリーにある任意の１枚のコマンドと同名のコマンドをリポジトリからワークツリーに加える.|
|find|リポジトリから任意のコマンドをワークツリーに加える.|
|mv|① ワークツリーにある任意の１枚のコマンドを相手コミッターのワークツリー又はリポジトリに移動する.<br>② ワークツリーにある任意の１枚のコマンドを相手コミッターのワークツリー又はリポジトリの任意の１枚のコマンドと交換する.|
|touch|自分又は相手コミッターはリポジトリから１枚引き, ワークツリーに加える.|
|rm|自分又は相手コミッターのワークツリーから１枚選択し, リポジトリに戻す.|
|mkdir|自分又は相手コミッターはリポジトリから３枚まで引き, ワークツリーに加える.|
|rmdir|分又は相手コミッターのワークツリーから３枚まで選択し, リポジトリに戻す.|
|sudo|自分又は相手コミッターに対して任意のコマンドを実行できる.|
|fork bomb|相手コミッターは2<sup>相手コミッターのワークツリー</sup>枚リポジトリからワークツリーに加える.|
|↑|前回実行したコマンドを再度実行する.|
|command + c|相手が実行したコマンドを無効化する.<br>このコマンドはこのゲームの中で唯一相手ターン中に実行できるコマンドである.|

# カード枚数
fork bombは２枚, その他のコマンドは４枚ずつの計50枚から構成される.
