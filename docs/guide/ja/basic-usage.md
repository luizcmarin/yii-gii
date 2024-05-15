基本的な使用方法
================

Gii にアクセスすると、最初に、ジェネレータを選択できるエントリ・ページが開かれます。

![Gii エントリ・ページ](../../images/gii-entry.png)

デフォルトでは、以下のジェネレータを利用できます。

- **モデルジェネレータ** - このジェネレータは、指定したデータベース・テーブルの ActiveRecord クラスを生成します。
- **CRUD ジェネレータ** - このジェネレータは、指定されたデータ・モデルの CRUD 操作 (作成・読み出し・更新・削除) を実装するコントローラとビューを生成します。
- **コントローラ・ジェネレータ** - このジェネレータは、新しいコントローラのクラスと、一つまたはいくつかのコントローラ・アクションおよびそれに対応するビューを迅速に生成するのを手助けしてくれます。
- **フォーム・ジェネレータ** - このジェネレータは、指定されたモデル・クラスのための、入力を収集するフォームを表示するビュー・スクリプトを生成します。
- **モジュール・ジェネレータ** - このジェネレータは、Yii のモジュールが必要とするコードのスケルトンを生成するのを手助けしてくれます。
- **エクステンション・ジェネレータ** - このジェネレータは、Yii のエクステンションが必要とするファイルの生成を手助けしてくれます。

"Start" ボタンをクリックしてジェネレータを選択すると、ジェネレータのパラメータを構成するためのフォームが表示されます。
あなたの要求を満たすようにフォームに入力して "Preview" ボタンをクリックすると、Gii が生成しようとしているコードのプレビューが出来ます。
選択したジェネレータや、既存のファイルの有無によって多少異なりますが、次の画像で見るのと同じような出力が得られます。

![Gii プレビュー](../../images/gii-preview.png)

ファイル名をクリックすると、そのファイルのために生成されるコードのプレビューを見ることが出来ます。
ファイルが既に存在する場合は、既存のコードと生成されるコードのどこが異なるかを示す差分ビューも提供されます。
その場合は、どのファイルを上書きし、どのファイルを上書きしないかを選択することも出来ます。

> Tip: データベースに変更を加えた後で、モデル・ジェネレータを使ってモデルを更新したい場合は、Gii のプレビューからコードをコピーして、あなたのコードに変更をマージすることが出来ます。
PHPStorm の [クリップボードと比較](https://www.jetbrains.com/help/phpstorm/comparing-files-and-folders.html) のような IDE の機能を使うと良いでしょう。
[Aptana Studio](https://www.aptana.com/products/studio3/download) や [Eclipse](https://www.eclipse.org/pdt/) ベースのエディタも [AnyEdit tools plugin](https://andrei.gmxhome.de/anyedit/) を使って [クリップボードと比較](https://andrei.gmxhome.de/anyedit/examples.html) をすることが出来ます。
この機能を使うと、関係のある変更だけを取り込んで、あなた自身のコードを取り消すような他の変更は放っておくことが出来ます。

コードをレビューして、生成すべきファイルを選択し、"Generate" ボタンをクリックするとファイルが生成されます。
すべてうまく行けば、これで終りです。
Gii がファイルを生成できないというエラーが出た場合は、ウェブ・サーバがファイルを作成してディレクトリに書き込むことが出来るように、ディレクトリのアクセス権限を修正しなければなりません。

> Note: Gii によって生成されるコードは、あなたの要求に従って修正すべきテンプレートに過ぎません。
  Gii は新しいものを素早く作成する手助けをするために存在するものですが、そのまま使用できるコードを作成するようなものではありません。
  Gii によって生成されたモデルを変更せずに、ちょっとした所だけを修正して使っている人をよく見かけます。
  これは、意図されている Gii の使い方ではありません。
  Gii によって生成されるコードは不完全であったり、間違っていたりする可能性があるもので、あなたの要求を満たすように変更して初めて使用できるようになるものです。