# dj2
https://zenn.dev/hathle/books/django-blog-book/viewer/01_ready

下には自分で詰また所をメモしていくスタイル
Chapter 02

1    GitHub
    
    新しいアカウントなのでssh接続とか繋げないと使えない
    いつも迷うところ
    参考
    https://qiita.com/GakuNaitou/items/81dbbd3ea6211af71648

    gitignore ファイルを追加
    これを忘れると次のpipで1000個以上ファイル出てくるのでビビる

2   仮想環境
    
    タイプミスしなければ楽勝　というかコピペが最強

3   最新 pip コマンド
    
    バージョン古いと色々揉める原因かと

4   パッケージ設定
    
    requirements.txt　作る
    一個づつ pip するのはやったらいけない

5   インストール
    上で作ったファイルを全部ダウンロードして組んでくれる


Chapter 03
１    Django の仕組み　料理に例えると
モデル	説明
Model	調理人
Template	盛り付け係
View	ウエイトレス

用語	ファイル	レストランで例える　
ルーティング	urls.py	URL 注文受付窓口
ビュー	views.py	盛り付け係
フォーム	forms.py	注文書いた伝票
モデル	models.py	調理人が冷蔵庫（データベース）から食材出して使う
テンプレート	xxx.html	客に出された料理



２    プロジェクト作成

    とりあえずコピペ

３    環境設定変更

    ファイルの場所の見方わからないとココで詰む
    ディレクトリとフォルダの見方教えてもらっとこう

    そして変更する場所は２８行目と１００行目あたり

４    データベースのセットアップ

    コピペ


    Web サーバーを起動する

    コピペのあと
    http://127.0.0.1:8000/
    行ってロケット出てたらここまではできた

Chapter 04

Django でアプリケーションを使えるように設定

コピペ

Chapter 05
    フィールドクラス

フィールドクラス	説明
ForeignKey	多対 1 の関係で他のモデルへのリンク
CharField	文字列のフィールド
TextField	多量のテキストのフィールド
DateTimeField	日付と時刻のフィールド
IntegerField	整数のフィールド
FloatField	小数のフィールド

    フィールドオプション

フィールドオプション	説明
null	データベースの NULL 可否を設定
blank	フォームフィールドのブランク可否を設定
choices	フォームの選択枠を設定
default	デフォルト値を設定
unique	ユニーク制約を設定
verbose_name	フィールド名を設定
validators	バリデーションの設定

    リレーションフィールドクラス
 
リレーションフィールドクラス	説明
OneToOneField	1 対 1
ForeignKey	1 対 多
ManyToManyField
 
    on_delete オプション

on_delete オプション	説明
models.CASCADE	一緒に削除される
models.PROTECT	削除できない
models.SET_NULL	NULL がセットされる
models.SET_DEFAULT	デフォルト値がセットされる
models.SET	任意の値がセットされる
DO_NOTHING	何もしない

    models

コピペ



