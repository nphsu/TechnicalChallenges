# What can I do?
自分は何ができるのか。自分が過去に何をやっていたか忘れないよう、使ったことのある技術あるいは体系的に学んだ技術を記録に残していく。

## 1. Frontend Programming

### React

モバイル向けWeb社内管理画面にて採用。`JSX`で記述。小さなアプリだったので`Redux`の採用は見送る。`React-Bootstrap`を使って画面のUIを装飾。タスクランナーには`Gulp`を使用。

### Vue.js

ウォレットシステムの社内管理画面で作成。UIコンポーネントは`ElementUI`を使用。`Webpack`で`npm`スクリプトを記載。`vue-router`を使ったシンプルな`SPA`構成。

シンプルな文法とドキュメントの豊富さから、キャッチアップコストを抑えて開発が可能であった。

### Nuxt.js

ユニバーサルなVue.jsのフレームワーク。個人で使用。

### Puppeteer


## 2. Backend Programming

### Java

大学４年生の秋に初めて学んだプログラミング言語。「やさしいJava」通称"やさJava"を３周して一通りのことが理解できるようになった後、200名規模のシステム会社でインターンを始める。再度Javaの研修が始まり、同時に`HTML`、 `CSS`、`JavaScript`の基礎を教わる。`Servlet`や`JSP`を使い、WebアプリケーションとしてJavaを使用する方法を２ヶ月の研修で習得。

その後、`Struts2`と`MyBatis3`を使ったECサイトを構築。`DBUnit`を使ったテスト自動化や、`jQuery`を使ったデザインなど、古い技術ではあったがプロダクションを作る上で必要になる知識を身につける。オブジェクト思考の基礎は、師匠である当時の開発部長にこの頃叩き込まれた。

インターン卒業後の社会人１年目でもJavaを使った研修からスタート。フレームワークを使わずにオブジェクト指向的なプログラムへのリファクタリングをする日々で新しいことは特に学ばなかったが、このころの繰り返しが今後のプログラミング習得にも生かされたと思う。暇すぎで学んだ関数型プログラミングの考えを実践するため、今まで書いたコードをJava8で実装直したりしていた。

同8月から初プロジェクトに参画。`SpringBoot`ベースのフルスクラッチ開発で、Springフレームワークや`JPA`、`Gradle`などのJava関連を学ぶ。

続くウォレットシステムの開発では、`Reactor`を実装した`SpringWebFlux`の導入に挑戦。既存技術との相性の悪さから１ヶ月で撤退したが、`Reactive Programming`に触れた経験は貴重だった。

### Node.js

ウォレットシステムのコア実装で使用。フレームワークとして`Express`を選択。ただし、Lambdaで使用する箇所はプレーンなNode.js8系で記述。`Async/Await`や`const/let`などの`ES6`記法やJavaScriptの関数型プログラミングはこの頃身につけた。テストは`Mocha`で作成。

その後、社内トークンシステムにてブロックチェーンとの接続部分をNode.jsで作成。また、同システムで`SlackAPI`との接続部分もNode.jsで記述するなど、この頃は「困った時はとりあえずNode.js」という感じだった。

### Go

ウォレットシステムのコア実装でGoを採用するためにサンプル実装を作成したのが初のトライアル。しかし、運用メンバ含むキャッチアップコストと、Node.jsと比べたコミュニティの未発達さに負けて採用は見送りに。

その後、一度Node.jsで作成した社内トークンシステムにてブロックチェーン接続部分とSlack接続部分をGoでリプレイス。Lambda+Goによるファンクションベースのマイクロサービス
とした。

### Rust

CやC++を経験していない自分にとって、システムプログラミングをしっかり学びたいという気持ちが強く、せっかくならと背伸びをして学び始めたのがRust。個人の〇〇プロジェクトで使用。メジャーどころを意識し、フレームワークは`Iron`、ORMapperは`Diesel`を選択。

### Python

機械学習を勉強中の知り合いエンジニアと一緒にWebサービスを作る時使用したのがPythonの`Django`。


## 3. Mobile Programming

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

## 7. Cloud

### AWS Elastic Beanstalk

社会人１年目の初プロジェクトで使用していたPaaS。この存在のせいで、インフラ観点の知識習得が遅れたと言っても過言ではないくらいアプリケーションエンジニアにとっては便利なサービス。サーバである`EC2`、LBである`ALB`、`Cloud Watch Logs`へのログ転送、画面から簡単にデプロイ可能、モニタリング、オートスケーリングなど、多くのことをマネージドにこなしてくれる心強い存在。ただ、構築時のトラブルシュートや機能拡張時に使用する`.ebextensions`は泥臭いので、自分で解決しようとなるとサーバやLBなどインフラ知識が結局必要になる。

アプリケーションとして Java / Node.js / Multi-container Docker をデプロイしていた。

### AWS Lambda

サーバレスFaaSの代表格。GoやNode.jsで構築していた。`API Gateway`と組み合わせて使うことで、サーバレスな`RESTful API`を簡単に構築できる。無料枠が管理大きく、メンテの不要なサービスをほぼ無料で利用できるという嬉しい側面がある。ただし、利用時間制限が5分と短く、VPC内で起動すると処理開始までに15秒くらい要する時があるので注意。

ローカル環境でLambdaを開発、デプロイするための`Serverless Application Model(SAM)`が用意されていて、コマンドを流すことでAPI Gatewayと共に`CloudFormation`を流してくれる。

### Amazon Elastic Container Service
### ElasticContainerServiceForKubernetes
### Cognito
### SQS
### SNS
### CodePipeline

### Firebase

## 8. Blockchain

### Ethereum

ウォレットシステムに携わる中で、Dapps開発の魅力を感じEthereumを深掘り。独自トークンを簡単に発行できる`ERC20`という規格をベースに、`MetaMask`でアドレス発行、`Truffle`でビルドデプロイ、`Remix`で開発（途中からTruffleをやめRemixに完全移行）、`Ganache`でローカル環境構築、`OpenZeppelin`というライブラリの使用など一通りのEthereum Dapps関連技術を独習。

キャラクターの保持可能が魅力となる`ERC721`に沿ってアイテム開発していたが、その後登場した`ERC1155`がERC20とERC721の両者を取り入れた規格であり、ERC1155を使用して社内トークンシステムのブロックチェーン部分を開発。

## 9. Game

### Unity(C#)

### SceneKit(Swift)

## 10. DevOps

### CICD

### Monitering

## 11. Architecture
### Serverless
### Microservices
### DomainDrivenDesign
### CleanArchitecture
