# 職務経歴書
2019年7月現在

## スキル
### 言語
|言語|経験歴|練度|
|:--|:--|:--|
|Ruby|3年|人に教えることができる|
|JavaScript（TypeScript）|3年|業務上問題なく使用することができる|
|HTML（slim, pug）|3年|業務上問題なく使用することができる|
|CSS（scss）|3年|業務上問題なく使用することができる|
|PHP|半年|業務で使用経験がある|

### フレームワーク/ライブラリ
|名称|経験歴|練度|
|:--|:--|:--|
|Rails|3年|人に教えることができる|
|Vue（Nuxt）|2年|業務上問題なく使用することができる|
|React|2年|業務上問題なく使用することができる|
|jQuery|1年|業務上問題なく使用することができる|

### その他（ツール）
|名称|経験歴|練度|
|:--|:--|:--|
|AdobeXd|1年|業務で使用経験がある|
|Sketch|1年|業務で使用経験がある|
|Photoshop|1年|個人で使用経験がある|
|Illustrator|1年|個人で使用経験がある|
|adobe premiera pro|1年|個人で使用経験がある|

## 制作物
自分の行きたい場所に対しての同行者を募集するwithruitというサービスを開発・運営しています。  
https://withruit.com  
リリースしてから1ヶ月で100人の初期ユーザを集めるためにやったことに関して、Qiitaにまとめました。  
https://qiita.com/hand12/items/2ea01a99b44a43235bb4  
よかったら見ていただけると嬉しいです。

2019/5/28に行われた、firebase meetup では、Nuxt × firebaseによるSSRなwebアプリケーションについてLTをしてきました。  
その際に「誰もが簡単にまるばつクイズを作成することができる まるばつクイズジェネレーター」というアプリを作成しました。  
「誰もが簡単に」ということで、UIに関して力を入れています。  
もしよかったらみていただけると幸いです。  
https://marubatsu-quiz-generator.web.app/  

友人と現地ガイドマッチングサービスも開発しました。  
https://factearth.net/  
デザイン、フロント、一部サーバーサイドを自分が担当し、友人がメインでサーバーサイドを担当して作成しました。  
こちらも、触って見た感想をいただけると嬉しいです。  

新婚旅行の方向けの旅行予約サービスのLPを作りました。  
デザイン・実装全て自分一人でやりました。  
こちらも見ていただけると嬉しいです。  
https://tokutabi.net  


## 登壇資料
Spreaker Deck  
https://speakerdeck.com/hand12_k


## 携わったプロジェクト（抜粋）

### 行きたい場所に対しての同行者を募集するサービス「withruit」の個人開発

行きたい場所に対して、一緒に行く相手を募集するサービス「withruit」を個人開発しました。  
https://withruit.com  

【サービスについて】  
自分が行きたい場所を投稿することによって、同行者を募集するサービスです。  
開発期間は2ヶ月弱で、リリース後は1ヶ月で初期ユーザを120人集めることができました。  
現在は、管理者機能からマークダウンで記事を入稿できる機能を作成し、サイト内に入稿した記事を表示できる機能を開発しています。  

【使った技術について】  
フロントはNuxt.js、バックエンドはfirebaseを使っています。  
React, Angular, Vueを一通り触ってみて、自分が一番素早くアプリケーションを作れそうだなと感じたVueを使ってアプリケーションを作成しました。  
また、ルーティングの自動生成やSSRのやりやすさなどの恩恵も受けたかったため、Nuxt.jsを使ってみました。  
バックエンドに関しては、今回作るアプリケーションがそんなに複雑な機能がないということと、個人サービスなのでなるべくコストを抑えたいという思いから、firebaseを使ってみました。

【苦労した点】  
* **初期ユーザ集め**  
すでに個人でいくつかサービスを作っていたこともあったため、アプリケーションの作成自体はとくに詰まることなく作ることができました。  
ただ、作ったアプリケーションを使ってくれるユーザーがなかなか集まりませんでした。  
そこで、bosyuや個人サービスをサイト上に掲載してくれるサイトに掲載依頼を出して、初期ユーザを集めることにしました。  
結果、冒頭でも書きましたがリリースから1ヶ月で120人を越える初期ユーザを獲得することができました。  

* **フロントに対する責務の分割**  
今回はNuxt.jsとfirebaseを使ってアプリケーションを開発したため、サーバーレスなアプリケーション構成を選択しました。  
そのため、普段はサーバー側でやっているような処理もフロント側で処理してしまい、フロントの責務を大きく超えてしまうような構成になってしまいました。  
そこで、今回はfirebaseのcloud functionsという機能を使い、フロントから少しづつ処理を分割して行きました。  
cloud functionsでは、データベースの変更や認証をトリガーに処理を実行できるので、フロントで持ちたくない関心ごとに関して、分割することができました。  

* **NoSQL形式によるデータ設計**  
データの永続化にfirebaseのrealtime databaseを使用したため、データはNoSQL形式で管理する必要がありました。  
今までRDBでのデータ設計経験しかなかったため、RDBに保存している感覚でアプリケーション開発を行うと、欲しいデータが取得しにくいということが多々ありました。  
そこで、NoSQL形式のデータ設計に詳しい方からアドバイスをもらい、多少冗長になってしまうものの、画面単位で欲しい情報を取得しやすいよう、データを保存するようにしました。  
その結果、用途別で同じデータを複数箇所で保持することになり、多少の冗長さは感じるものの、なんとかデータの取得ロジックをシンプルに保ちながら、欲しい情報を取得できるように実装できました。  



### レガシーだった契約管理をシステム化する

【プロジェクト概要】  
自社サービスに対する契約を管理するシステムの構築。  
* **背景**  
自社で開発・運営されていたtoB向けのサービスに関して、契約を紙 or スプレッドシートで管理していた。  

* **課題**  
サービスを運営していくにつれて、商品の数が増えたり、関わる部署が増加し、スプレッドシートでの運用が厳しくなってきた。  
また、IT統制の観点でも契約書に基づいたサービスの提供をシステムで管理する必要も出てきた。  

* **解決策**  
業務フローに合わせた契約管理ツールを作成するという方針になった。  
しかし、システム開発にかける時間もリソースも限られていたため、0から構築するのではなく、すでに用意された様々なツールやサービスを使って、システムを構築することにした。  
これらと、既存の業務フローを考慮し、下記のツールを使ってシステムを構築することにした。  
  - kintone
    - cybozuが提供している「業務ツールをクラウド上で高速に作成できるサービス」
    - JavaScriptで細かなカスタマイズが可能
  - GCP Cloud Functions
    - googleが提供しているサーバレスで関数を実行する環境を提供してくれるツール
    - 自分でサーバーを構築せずに、様々な処理を実行することができる
その結果、システム開発にかかる時間やリソースを大幅に削減し、システムを構築することができました。  

【担当した内容】  
作成した契約管理システムと基幹システムを連携する箇所の設計・実装  

自社サービスに顧客から申し込みが来た場合、cloud functionsを通じてkintoneへ情報が同期される仕組みを作成した。  

【苦労した点】
* **エラー検知**  
契約情報を扱うため、データの棄損は許されない。  
そのため、エラーが発生した場合は速やかに通知し、対処する仕組みを構築する必要がある。  
今回は、顧客が申し込みを行った場合、GCPのCLOUD PUB/SUBにキューを積み、サブスクライバーとして指定したcloud functionsがキューを処理するという実装にしていました。  
cloud functionsにはstack driverという処理中に発生したエラーを検知する機能があったので、今回はこちらを使いました。  
ただ、stack driverのエラー通知の仕組みが以下の理由で使えなかったため、自前で作成することにしました。  
  - **slack通知**  
      - 弊社のルールで、slack公式のアプリケーション以外を社内のslackに導入することができない
      - 当時、stack driverが提供しているslack通知用のアプリケーションは、slack公式のアプリケーションではない。
  - **メール通知**  
      - エラーを検知した場合、特定のメールアドレスにエラーを通知する機能は提供されている
      - 弊社が用意しているGSUITのアカウントではメールの転送機能が使えない。

  そこで今回は、エラーを検知した場合、エラー内容をCLOUD PUB/SUBにキューとして積んで、cloud functionsでslackに通知する。という手段を選びました。  
  管理するコードが増えたので、管理コストが上がる懸念はあったものの、自由度が高いエラー検知の仕組みを作成することができました。  

* **kintone開発**  
cybozuが提供するkintoneでは、比較的容易に業務システムを構築することができるのですが、今回は基幹システムとの連携が必要だったため、追加で開発を行う必要がありました。  
kintoneではJavaScriptを使って機能を拡張することができます。  
また、自分たちのチームでは、型安全の恩恵などを受けたくTypeScriptを、用いて開発を行っていました。  
しかし、kintoneとTypeScriptを組み合わせている事例は当時なかなかなく、型データやドキュメントもあまりない状態でした。  
そこで、kintoneにおけるTypeScriptでの開発事例やノウハウを吸収すべく、積極的にkintoneのイベントに出席するようにして、知見の吸収や共有を行うようにしました。  

### 自社で運営している転職エージェントが持つ案件を、自社サービス上に転載するプロジェクト

【プロジェクト概要】  
自社で運営している求人サイトに、同じく自社で運営している転職エージェントが持つ案件を転載するプロジェクト  
転職エージェントのグループでは、案件を他社が提供しているクラウドサービスを利用して管理しているため、日時で案件情報を書き出し、自社のDBに保存するためのバッチを作成しました。  

* **背景**
  - 弊社では、求人バーティカルサイトを運営しているため、いくつかの企業から求人情報をいただき、サイト上に掲載している
  - 各提携先企業から様々なフォーマットで提供される求人情報を、PHPで実装されたバッチで自社サービスのDBに格納するようにしている
  - サービス開始当初から可動しているバッチであり、開発に携わっていた人も殆ど社内に残っていない
  - 今回転載する転職エージェントが持つ案件も、システム上これら同じ求人情報として扱う必要がある

* **課題**
  - 現状の実装だと、同じバッチの中で全ての提携先企業の求人情報を取り込むようになっており、処理時間がかなりかかっている。（1時間弱）
  - 提携先で問題が発生した場合、バッチを再度実行する必要があったため、全ての提携先の求人情報を取り込み直す必要がある
  - 新しい取り込みバッチを作成するにあたって、既存のバッチと同じDBに保存する必要があるが、既存のバッチではMySQLのオートインクリメントを使わない実装になっているため、同時に実行すると整合性が取れなくなる

上記の問題を踏まえて、以下の用に実装・設計しました。
* 提携企業毎に処理を分割し、手動で個別にデータのインポートができる
* 新規で作成するバッチの開始時に、MySQLにロックを掛けて既存のバッチ処理と同時に書き込まれることがないようにする

これらにより、既存の取り込みバッチに影響を与えないようデータを取り込むよう設計・実装しました。  

【担当した内容】  
プロジェクトリーダーとして、プロジェクト全体の進捗管理を担当しました。  
また、開発者としてもチームに参画し、設計や要件定理をメンバーと協力して行いました。  

【苦労した点】  
初めてのプリジェクトリーダー経験だったということもあり、以下のようなことに苦労しました。  
- 進捗共有の資料など、非エンジニアの人にもわかりやすいような言葉で説明すること
- 開発以外の作業
  - 開発に必要な資料の作成
  - ツールの開発要アカウントの準備
  - 関係者との日程調整
- スケジュール管理
  - 遅延を懸念しすぎて、バッファをかなり多めにとってしまった

## 職務経歴

期間：2017年6月〜2017年12月  
役割：開発者  
内容：社内システムの保守・機能追加  
言語：Ruby（Rails）, TypeScript（React）  
概要：自社サービスの機能追加であったり、お問い合わせ対応など。  

期間：2017年1月〜2018年6月  
役割：開発者  
内容：契約管理システムの構築  
言語：TypeScript（GCP cloud functions, kintone）, Ruby(Rails)  
概要：紙やspreadsheetで管理されていた契約情報をシステム化するプロジェクト。技術選定、実装を担当。  

期間：2018年7月〜2018年9月  
役割：開発者  
内容：社内製のメールサーバーにおける保守・機能追加  
言語：TypeScript（GCP cloud functions, kintone）, PHP  
概要：PHPで実装されていた社内製のメールサーバーをTypeScriptで実装された基盤に移行。こちらでは実装のみを担当。  

期間：2018年10月〜2018年12月  
役割：開発者  
内容：基幹システムの保守・機能追加  
言語：Ruby（Rails）  
概要：toB向けの自社サービスの機能追加、お問い合せ対応を担当。  

期間：2019年1月〜2019年3月  
役割：プロジェクトリーダー・開発者  
内容：転職エージェントグループが持つ求人案件の転載  
言語：Ruby（Rails）  
概要：エージェントグループが管理している案件をweb上に公開し、一般のユーザーにも見れるようにするプロジェクト。今回ははじめてのプロジェクトリーダーとして、スケジュール管理やタスクの分割、関係者との調整を行った。  

期間：2019年4月〜2019年6月  
役割：開発者  
内容：自社サービスのグロースハックプロジェクト  
言語：Ruby（Rails）, PHP, JavaScript（React）  
概要：自社サービスのグロースハック施策を行うプロジェクト。メンバー全員で分析、施策の立案、実装を行った。  
