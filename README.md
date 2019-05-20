# レッスン1. 初めてのReact

## Reactとは

![react_official](https://firebasestorage.googleapis.com/v0/b/codegrit-images.appspot.com/o/codegrit-react%2FLesson01%2Freact_official.png?alt=media&token=d0be04b9-5527-42ee-8cf0-ed0c844dea18)

ReactはUI(ユーザーインターフェース)を構築するためのライブラリ(UIライブラリ)です。Facebookによって作成され、メンテナンスされています。最初のリリースは2013年5月とまだ新しいのですが、世界中の多くのサービスで採用されております。

## Reactを利用しているサービスの例

![react_companies.png](https://firebasestorage.googleapis.com/v0/b/codegrit-images.appspot.com/o/codegrit-react%2FLesson01%2Freact_companies.png?alt=media&token=23583e38-43ad-498b-87f4-7f844083f4e3)

Reactは開発元のFacebookだけでなく世界中の有名企業で利用されています。例えばFacebook子会社のInstagram、そしてPayPalやTwitter、日本だとリクルートもReactを採用しています。

## Reactを学ぶメリット

上述の通りReactはリリースが2013年とまだ新しいライブラリです。また進化のスピードが早くリリースから現在のバージョン16まで多くの新機能が追加されてきました。そのため、需要に対してまだ供給が足りていません。

また、これまでのフロントエンド開発では、難しいことはサーバー側で行いフロントは難しいことは行わず、jQueryのようなライブラリを使い、少しだけ動きを出すというのが普通でした。そのために、フロントエンド開発には本格的なプログラマは元々数が多くありませんでした。

これらの理由からReactを知っていれば<u>仕事の機会が豊富</u>にあります。また自分でサービスを作るのであれば、他のサービスに加えてより<u>ユーザーエクスペリエンスに優れたサービスを作りやすい</u>と言えます。

## なぜReactを使うのか

Reactを利用して開発する大きな理由は以下の3つです。

- **コミュニティが大きい**
- **状態を明確にしやすい**
- **高速**

その他にも、React Nativeというライブラリを利用すると、iPhoneやAndroid用のアプリを作ることが出来ることもメリットと言えます。

### Reactのエコシステム

![react_ecosystem.png](https://firebasestorage.googleapis.com/v0/b/codegrit-images.appspot.com/o/codegrit-react%2FLesson01%2Freact_ecosystem.png?alt=media&token=6c60f38f-b285-4aeb-88df-940919cec815)

Reactの開発元、及びメンテナーはFacebookです。そのため、小さな会社やコミュニティによってサポートされているツールに比べて<u>信頼性が高い</u>といえます。

コミュニティの大きさはアプリを作成する上で非常に重要です。コミュニティによって作られたライブラリがなければ、必要なライブラリを自分で実装しなければいけないケースが増え開発スピードが落ちてしまいます。

この点で、Reactはオープンソースコミュニティの規模も最大級で、ReaduxやReact RouterなどReactを拡張するためのライブラリが多くあります。こうしたライブラリを利用することでより<u>早く安定してアプリ開発を行うことが出来ます</u>。

### Componentべース

HTML/CSSコースを受講した方であれば、既にコンポーネントの考え方には慣れ親しんでいるかと思います。Reactでは、一つの画面に存在する様々なパーツをReactコンポーネントとして作成していきます。このようにパーツごとに分けることで全体のコードの見通しが良くなります。また一つのコンポーネントを再利用することが可能となり様々なページで一貫したUI(ユーザーインターフェース)を提供することが可能となります。

### Virtual DOM

Virtual DOMとは、名前の通りブラウザのDOMを仮想的に表現するものです。Virtual DOMはアプリケーションとDOMをつなぐレイヤー的な役割を担っています。

Reactは直接DOMを操作するのではなく、このVirtual DOM上にブラウザ上に表示する情報を保持しており、何らかのイベントで表示を変更する際にはこのVirtual DOMへの反映後、最終的に実際のブラウザのDOMを変更します。

このように中間のレイヤーを挟むことによって直接DOMを操作するよりも高速な表示の変更を可能にしています。

## jQueryとの違い

jQueryはもともと、異なるブラウザ間でのJavaScriptファンクションの違いに対応するために作られました。しかし、現在では主要ブラウザ間での違いは少なくなってきており、また最も違いの大きかったマイクロソフト製のブラウザもGoogleの公開するオープンソースのブラウザ「クロミウム」をベースにすることが発表されています。これによってもともとのjQueryが担っていた役割は終わったと言われています。

またjQueryは様々なファンクションをより簡潔な名前で呼び出したり、DOMの取得を簡単にできますが、それらを構造的に管理することは困難でした。そのため、フロントエンド側での処理が以前に比べて多くなっている現在ではReactやVueのようなコンポーネントベースのライブラリがより適しています。

ただし、jQueryは歴史が長く様々なオープンソースのツールが公開されています。あまりフロントエンドが複雑でない場合の開発では、Reactなどを利用するよりもjQueryとそれらのツールを組み合わせたほうが開発スピードを上げられることも多いと言えます。

## create react appを利用する

Reactを利用するには、BabelやWebpackを利用してReactのコードをES5のコードにトランスパイル必要があります。こうした下準備は自分で行っても良いのですが、初心者には大変です。

Facebookではこの問題を解決するために、create-react-appというライブラリを公開しています。このライブラリを利用することで、多くのベストプラクティスに沿いながらReactでのアプリ開発を簡単に開始することができます。

CodeGritでは基本的にこのcreate-react-appを全面的に採用して使っていきます。

## create react appでアプリを作成する

GitHub上の[公式ページ](https://github.com/facebook/create-react-app)上の指示にしたがってcreate react appのアプリを作成します。

```bash
$ npx create-react-app hello-world
```

すると、hello-worldというアプリが自動的に作成されます。作成されたアプリのディレクトリに移動し、`yarn start`とすればすぐに開発がスタートできます。上手く行かない場合は`yarn run start`を試してください。

```bash
$ cd hello-world
$ yarn start
```

"http://localhost:3000/" を開いてみて、以下のような画面が表示されていればアプリの立ち上げ成功です。


## Hello World

さてアプリが作成できたので編集していきましょう。今回は簡単に"Hello World"とページ上に表示するだけのシンプルなアプリを作っていきます。まずは、create react appで作成されたフォルダーの中身を見てみましょう。srcフォルダを開くと以下のようなファイル構成になっているはずです。

├── App.css
├── App.js
├── App.test.js
├── index.css
├── index.js
├── logo.svg
└── serviceWorker.js

これがcreate react appを利用してReactアプリの基本的な構成となります。

ご覧になって気づく通り、Appというファイル名を持つファイルが3つ(App.css, App.js、App.test.js)あります。App.test.jsはApp.jsをテストするためのファイルです。App.cssは後々説明しますがApp.js独自のスタイルを設定するためのファイルとなります。また最初に読み込まれるルートファイルであるindex.jsを除いて**ファイル名の最初には大文字**を使ってReactコンポーネントであることを示すのが一般的となっています。

App.jsの中ではアプリ全体で必要な設定の読み込みなどを行うのが一般的です。そして、index.jsを利用してApp.jsや他のファイル情報を表示します。

serviceWorker.jsについては、JavaScriptのService Workerという仕組みを利用するためのファイルなのですが、今は気にしなくても大丈夫です。

さて、現状は "http://localhost:3000/" 上で表示されている画面のコードがすでに書かれているのですが、ここからアプリを一から作っていきますので、一旦App.jsとindex.jsの中身をすべて消してしまいましょう。今回は非常に簡単なアプリなのでindex.jsのみを利用していきます。

### React.createElement

では、最初にindex.jsを開きましょう。最初にすべきことはReactパッケージのインポートです。こうすることでReactエレメントやReactコンポーネントを作成することが可能となります。

```js
import React from 'react'
```

次にVirtual DOMへと反映するための要素`React要素`を作成していきます。この`React要素`は以下のようにして作ることができます。

```js
React.createElement('要素名', 'Props(プロパティ)', `子要素`)
```

これを利用して"Hello World"と表示するh1要素を作ってみましょう。

```js
import React from 'react'

const h1 = React.createElement('h1', null, 'Hello World')
```

これで、Virtual DOMに反映するためのh1要素を作成できました。

### ReactDOM.render

さて、要素を作成しましたが現状だとブラウザには何も表示されません。ブラウザにこの要素を反映するためにはReactDOMというライブラリを通して行います。

まずはpublicフォルダを見てみましょう。publicフォルダ内にindex.htmlというファイルがあるかと思いますので開いて見てください。すると以下のようになっているはずです。

```html
<!DOCTYPE html>
<html lang="en">
  ...省略
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
    ...省略
  </body>
</html>
```

ここで`<div id="root"></div>`の部分に注目してください。ReactDOMを利用することでこのdiv要素以下にVirtual DOMを通して反映されるDOM要素を表示することができます。

これを行うためには以下のようにします。

```js
const rootEl = document.getElementById('root') // Reactエレメントやコンポーネントを表示したいルート要素を取得
ReactDOM.render('反映する要素', rootEl);
```

このようにReactコンポーネントや要素を表示したい場所さえ取得すればページのどこにでもReactを利用することができます。

実際に、先程作成したh1要素を反映するためには以下のようにします。

```js
import React from 'react';
import ReactDOM from 'react-dom';

const h1 = React.createElement('h1', null, 'Hello World');
ReactDOM.render(h1, document.getElementById('root'));
```

再度 "http://localhost:3000/" を開いてみましょう。Hello Worldと表示されていれば成功です。

![hello_world](https://firebasestorage.googleapis.com/v0/b/codegrit-images.appspot.com/o/codegrit-react%2FLesson01%2Fhello_world.png?alt=media&token=3e263d98-fd62-4833-b12f-b7e1709b0023)

### Reactコンポーネントの作成

さてここまでは、作成したReactエレメントを直接反映するようにしたのですが、実際のReactアプリではコンポーネント、特にAppコンポーネントを反映することが一般的です。

Reactコンポーネントを作成する方法はいくつかあります。これらについてはレッスン2で詳しくみていきます。ここでは最も一般的なclassを利用した作成方法を試してみましょう。

App.jsを開いて以下のように記述してください。

```js
import { createElement, Component } from 'react'

class App extends Component {

  render() {
    const h1 = createElement('h1', null, 'Hello World');
    return h1;
  }
}

export default App;
```

これで最も基本的なReactコンポーネントが完成しました。classを利用してReactコンポーネントを作成する際には上記のように必ずrenderというファンクションを記述する必要があります。このrenderファンクションの内容がVirtual DOM上に反映されることとなります。renderの中身は先程のindex.jsとほとんど同じですね。

さて、次にindex.jsを変更してこのAppコンポーネントをReactDOM.render上で表示するようにしましょう。

```js
import React, { createElement } from 'react';
import ReactDOM from 'react-dom';
import App from './App'

const RootReactElement = createElement(App, null, null); //AppコンポーネントをReact要素にする。

ReactDOM.render(
  RootReactElement,
  document.getElementById('root'));
```

このようにComponentを呼び出す際も、createElementファンクションを利用する必要があります。

再度 "http://localhost:3000/" を開いてみましょう。先程と同様にHello Worldと表示されているはずです。

### プロパティ(Props)を渡す

さて、最後にもう少しだけ前に進みましょう。先程のReact.createElementの説明の部分で2つ目の引数に”プロパティ"とあったのを覚えているでしょうか？ Reactではこのプロパティのことを一般的に"Property"を省略して"Prop"と言います。またプロパティは一つではなく複数指定できますので`Proos`とsをつけて複数形で言うことが普通です。Reactでは、あるエレメントやコンポーネントからその子要素に当たる要素に対して、様々なPropsを引き渡して表示を操作することができます。ここでは"Hello World"のWorldの部分をPropsを利用して変更できるようにしてみましょう。親要素、親コンポーネントから渡されたProposには、`this.props`でアクセスすることができます。

AppWithProps.jsというファイルを作成して、以下のように編集しましょう。先程のApp.jsに似ていますが、親から渡されたpropsを利用しています。

```js
import { createElement, Component } from 'react'

class AppWithProps extends Component {

  render() {
    const word = this.props.word // 親要素から渡されたPropsからwordプロパティを読み込む。
    const h1 = createElement('h1', null, `Hello ${word}`);
    return h1;
  }
}

export default AppWithProps;
```

更にindex.jsからAppコンポーネントにPropsを渡すようにします。

```js
import React from 'react';
import ReactDOM from 'react-dom';
import AppWithProps from './AppWithProps'

const RootReactElement = React.createElement(AppWithProps, { word: '世界"' }, null)
ReactDOM.render(RootReactElement, document.getElementById('root'));
```

再度、ブラウザを開いてみましょう。"Hello 世界"と表示されていれば成功です。

![hello_sekai](https://firebasestorage.googleapis.com/v0/b/codegrit-images.appspot.com/o/codegrit-react%2FLesson01%2Fhello_sekai.png?alt=media&token=93fdfb65-471d-42fb-88a5-3157cbdf589b)

Propsについては、レッスン3以降について更に詳しく見ていきますがまずは、Propsを渡すことで子要素や、子コンポーネントの表示を変更することができるということだけ覚えておきましょう！

## サンプルコード

このレッスンで利用したコードはこちらのリポジトリよりご覧いただけます。create-react-appを利用しているので`yarn run start`で立ち上げられます。

[react-lesson01-sample](https://github.com/codegrit-jp-students/codegrit-react-lesson01-samples)

## 更に学ぼう

Reactの関する情報は、公式サイトが最も正確です。ブログ記事など公式以外の情報を参照する際には利用されているReactのバージョンを確認し、出来るだけ最新のバージョンに近い情報を選びましょう。

- [React公式サイト(日本語)](https://ja.reactjs.org/)
Reactの公式サイトの一部のドキュメントは日本語で読めます。ただし、変化の激しいライブラリなので最新の情報については英語のブログを読む必要がある場合もあります。
- [create-react-app公式サイト](https://facebook.github.io/create-react-app/)