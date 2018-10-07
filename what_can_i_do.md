# What can I do?
私は何ができるのか。自分が過去に何をやっていたか忘れないよう、使ったあるいは学んだ技術を記録に残していく。

## 1. Frontend Programing

### Vue.js

仮想通貨ウォレットシステムの社内管理画面で作成。UIコンポーネントは`ElementUI`を使用。`Webpack`で`npm`スクリプトを記載。`vue-router`を使ったシンプルな`SPA`構成。

### Nuxt.js

### Puppeteer

## 2. Backend Programing

### Java

大学４年生の秋に初めて学んだプログラミング言語。「やさしいJava」通称"やさJava"を３周して一通りのことが理解できるようになった後、200名規模のシステム会社でインターンを始める。再度Javaの研修が始まり、同時に`HTML`、 `CSS`、`JavaScript`の基礎を教わる。`Servlet`や`JSP`を使い、WebアプリケーションとしてJavaを使用する方法を２ヶ月の研修で習得。

その後、`Struts2`と`MyBatis3`を使ったECサイトを構築。`DBUnit`を使ったテスト自動化や、`jQuery`を使ったデザインなど、プロダクションを作る上で必要になる知識を身につける。オブジェクト思考の基礎は、師匠である松本さん（当時の開発部長）に叩き込まれた。

インターン卒業後の社会人１年目でもJavaを使った研修からスタート。フレームワークを使わずにオブジェクト指向的なプログラムへのリファクタリングをする日々で新しいことは何も学ばなかったが、このころの繰り返しが今後のプログラミング習得にも生かされたと思う。暇すぎで学んだ関数型プログラミングの考えを実践するため、今まで書いたコードをJava8で実装直したりしていた。

同8月から初プロジェクトに参画。`SpringBoot`ベースのフルスクラッチ開発で、Springフレームワークや`JPA`、`Gradle`などのJava関連を学ぶ。

続く仮想通貨ウォレットシステムでは、`Reactor`を実装した`SpringWebFlux`の導入に挑戦。既存技術との相性の悪さから１ヶ月で撤退したが、`ReactivePrograming`に触れた経験は貴重だった。

### Node.js

仮想通貨ウォレットシステムの仮想通貨コア実装で使用。フレームワークとして`Express`を選択。ただし、Lambdaで使用する箇所はプレーンなNode.js8系で記述。`Async/Await`などの非同期プログラミングやJavaScriptの関数型プログラミングはこの頃身につけた。

その後、社内トークンシステムにてブロックチェーンとの接続部分をNode.jsで作成。また、同システムでSlackとの接続部分もNode.jsで記述するなど、この頃は困った時はとりあえずNode.jsで記載していた。

### Go

仮想通貨ウォレットシステムのコア実装でGoを採用するためにサンプル実装を作成したのが初のトライアル。しかし、キャッチアップコストとNode.jsと比べたコミュニティの未発達さに負けて採用は見送りに。

その後、一度Node.jsで作成した社内トークンシステムにてブロックチェーン接続部分とSlack接続部分をGoでリプレイス。Lambda+Goによるファンクションベースのマイクロサービス
とした。

### Rust

CやC++を経験していない自分にとって、システムプログラミングをしっかり学びたいという気持ちが強く、せっかくならと背伸びをして学び始めたのがRust。個人の〇〇プロジェクトで使用。メジャーどころを意識し、フレームワークは`Iron`、ORMapperは`Diesel`を選択。

### Python

機械学習を勉強中の知り合いエンジニアと一緒にWebサービスを作る時使用したのがPythonの`Django`。


## 3. Mobile Programing

### Swift

ARKitを使えばARアプリを簡単に作れるらしいという話を聞いてMacbookProを購入し、iOS開発なので当然Swiftを選択。`Cocoa`を使ったパッケージ管理やGoogleMapSDKなどを使用しておもちゃレベルのアプリケーションを作成。コンセプトを決めてから3日間でAppStoreにARアプリをリリース。

### Kotlin

ARCoreを使えばARアプリを簡単に作れるらしいという話を聞いて使ってみたが、Android端末を個人で持っていない自分には長続きはしなかった。

SpringBoot2がKotlinを公式サポートしたことを機に、社内のJavaシステムをKotlinに置き換える運動をしてみたが失敗。

### Flutter


## 4. Database

### MySQL/MariaDB

研修時に使ったOracleDatabaseを除いて、今までつくってきたシステムほぼ全てがMySQLをメインに動いている。MySQLで困ったことは性能テスト時のページング処理、どうやら20ページ目のデータを取得する場合は20ページまでの全データを取得して19ページまでのデータを切り捨てる方式としているらしい。(MySQL5.6/5.7)

フェイルオーバの問題でうまく動作しないバグがあることがわかり、ドライバをMariaDBに切り替えたが、使用感およびパフォーマンスでほとんど違いがわからなかった。

大学４年時の研修と社会人１年目の研修で、MySQL用SQLとOracle用SQLのコマンドを練習。その後ネイティブSQLを直接書く機会はあまりなく、`JPQL`や`JPA`で抽象化されたものを利用していた。

### Aurora

MySQLベースでローカルを構築し、本番ではAWSのAuroraを使って性能向上を狙った導入が多かった。

### Redis

クラウドでアプリケーションサーバを構築する際、ステートレスな設計を心がけるが、セッション情報は保持する必要があったため、Redisでセッション情報を格納するために使用。また、マスタデータ等はRedisのデータを読みに行くことで、MySQL等から取得するよりも高速に動作することを目指した利用も一部採用。

Java欄で記載した`Spring WebFlux`で`ノンブロッキングIO`を目指すために`Reactive Redis`を採用。ただ、WebFlux採用見送りと同時にReactive Redisも見送りとなった。

### MongoDB
### DynamoDB
### Neptune

## 5.　ApplicationInterface

### REST
### GraphQL
### JSON-RPC
### gRPC

## 6. Containers
### Docker Compose
### Docker Swarn

### Kubernetes

## AWS
### ElasticBeanstalk
### Lambda
### ElasticContainerService
### ElasticContainerServiceForKubernetes
### Cognito
### SQS
### SNS
### CodePipeline

## Firebase

## 7. Blockchain

### Ethereum
- ERC20/ERC721/ERC1155

## 8. AR
### Unity(C#)
### SceneKit(Swift)

## 9. DevOps
### CICD
### Monitering

## 10. Architecture
### Serverless
### Microservices
### DDD
### CleanArchitecture
