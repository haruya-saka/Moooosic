
https://github.com/haruya-saka/Moooosic/assets/127200853/ca7132d6-319b-4787-85db-6c74adf21027
# Mooooosic（むーじっく）

[![IMAGE ALT TEXT HERE](https://jphacks.com/wp-content/uploads/2023/07/JPHACKS2023_ogp.png)](https://www.youtube.com/watch?v=yYRQEdfGjEg)

## リポジトリURL
フロントエンド：[(フロントエンドページ)](https://github.com/mooooosic/SubmitFrontend)

バックエンド：[(バックエンドページ)](https://github.com/mooooosic/SubmitBackend)
## 製品概要
### 背景(製品開発のきっかけ、課題等）
多くの音楽再生プラットフォームを私たちは使用しています。その中で、私たちの音楽体験の形というのが、均一化されているという問題があると考えました。多くの人が各プラットフォームで、プレイリストを再生するというような既存の形に縛られています。その中で、音楽×テクノロジーを掛け合わせ、自分の気分に適した音楽を再生することで、新たな音楽体験が可能であると考えました。
### 製品説明（具体的な製品の説明）


## ホーム画面
![ホーム画面](https://github.com/jphacks/SP_2301/assets/115796549/ef24b7b8-f716-4c4a-b92d-883c1958a655)
### ・撮影機能
ホーム画面の撮影を始めるというボタンを押すことで、撮影画面へと遷移することができます。
## 撮影画面
![撮影画面](https://github.com/jphacks/SP_2301/assets/115796549/2f279219-c518-4fad-ae8e-a80e4641f360)
撮影画面ではreactのweb-camを使用することで、写真の撮影を行います。写真の撮影が終了した場合、確認画面に遷移することができます。
## 確認画面
![確認画面](https://github.com/jphacks/SP_2301/assets/115796549/498d9e70-4d60-4044-b550-a63494f12858)
確認画面では撮影した写真を感情分析に使用するかどうかを確認します。取り直すを選択した場合は再び確認画面へ、感情を分析するを選択した場合はバックエンドに画像のバイトをpostします。リターンを受け取ったのち、ロード画面へと遷移、リクエストの値を渡します。
## ロード画面①
![ロード画面①](https://github.com/jphacks/SP_2301/assets/115796549/9c6fba75-7c83-41ac-9bc9-6c37a9cfaa6c)
確認画面から渡されたリターン（判定された感情）をバックエンドにpostする。バックエンドで感情に適した曲を10曲選び、リターンとして返す。その後、ローディング画面②に遷移する。
## ロード画面②
![ロー画面②](https://github.com/jphacks/SP_2301/assets/115796549/a48342ef-e800-44f8-8213-c02c001b98df)
ロード①の画面をフェードアウトさせ、ユーザーの感情を伝える。数秒間停止したのち、再生画面へ遷移する。
## 再生画面
![曲再生画面](https://github.com/jphacks/SP_2301/assets/115796549/3e2aebb4-b775-41e3-83c4-6b6f8146d27b)
バックエンドから受け取った、videoIDをもとにyoutubeの画面を表示し、再生を行えるようにする。また次へのボタンを押したら、videoIDを次のものに変更する。

### 特長
#### 1. APIを利用した感情判定
googleのcloud vision API を用いることで、表情の感情判定を行った。感情は「happy,agry,sad,surprise」の四パターンに分類される。
#### 2. デザイン
デザインにこだわって作成しました。ロゴやボタン、背景や感情の顔などもすべて自分たちで自作しました。
#### 3. 安価な曲再生
色々な曲再生のAPIを検討しましたが、どれも私たちやユーザーがいくらかの金銭的負担が生じました。そこでYouTube使用することで、金銭的な負担なく曲の再生を行えるようになりました。

### 解決出来ること
上記により手軽に気分の判定を行い、曲の再生が行えます。新たな形の音楽体験を提供することができます。
### 今後の展望
今回は顔の表情のみで、感情の判定を行いましたが、声（音声）や言葉（自然言語）を用いて、マルチモーダルな感情判定を行いたいです。
### 注力したこと（こだわり等）
* デザイン
メンバー全員がCSSの初心者でしたが、ボタンや画像の配置などをこだわりました
* 初めて参加するハッカソン
メンバーの4/5が初めてのハッカソンでしたが、デモでも通して動くようになりました。

## 開発技術
### 活用した技術
#### API・データ


* cloud vision API
* spotify API
* youtube iframe 

#### フレームワーク・ライブラリ・モジュール
* javascript
* react
* python
* flask
* web-cam 


### 独自技術
#### ハッカソンで開発した独自機能・技術
* 特に力を入れた部分をファイルリンク、またはcommit_idを記載してください。
* src/component/Load.js
ローディング画面
* server.py
バックエンド処理
