# react-study

## React入門


1. `npm install -g create-react-app`: Facebook製のReactアプリのスケルトン
1. `create-react-app test` : test プロジェクトの作成
1. `cd test` : test ディレクトリに移動
1. `npm start` : ブラウザ内でアプリが確認できる（http://localhost:3000）

## 変数宣言

ブレス``{}``を使って変数を表示することができる。


（varではなく）const, letは ECMA Script2015 から使える変数宣言(通常ブラウザでは動作しないがbabelが翻訳してくれている)。

const は代入不可能な変数、letは は代入可能な変数。コンパイルは通るがブラウザ内でエラーとして表示される。

## HTMLとJSXの違い(予約名と例外)

``<div className="ImageBox">`` というようにHTML/CSSのクラスは ``className`` と書く（JavaScriptのclassと被るため）と、生成されたHTMLでは``class``に置き換えられる。

``label`` 要素の ``for`` 属性は ``htmlFor`` と書く（ ``for`` に変換される）

## 独自属性

``<div hoge="">`` といった属性を付けたいときは ``<div data-hoge="">``と書く。そうしないと無視されて生成されたHTML上では消滅する。
JSXの変数名は基本はすべて ``lowerCamelCase`` 形式で書くが、 ``aria-*``, ``data-*`` のみ自由書式。

## HTMLのエスケープ処理

通常は文字列内のHTML要素はエスケープされる（＝クロスサイトスクリプティングなどを防ぐために、ltなどに変換される）。
以下のように書くことで、エスケープをせずにHTMLとして扱うことができる。

``someHtml = {__html: '<h2>これはH2要素</h2>' };``

``dangerouslySetInnerHTML={someHtml} ``




