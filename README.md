# kubernetes-perfect-guide

## chapter01のコマンド
 * docker image build -t sample-image:0.1
 * docker image build -t sample-image:0.2 -f Dockerfile-MultiStage .
 * docker image build -t sample-image:0.3 -f Dockerfile-Scratch .
 ## Dokcer Hub
  * [Dokcerレジストリのホスト名]/[ネームスペース]/[リポジトリ]:[タグ]
   * Docker Hubへのログイン
   * docker login
   * docker image tag sample-image:0.1 DOCKERHUB_USER/sample-image:0.1
   * docker image push DOCKERHUB_USER/sample-image:0.1
   * docker logout
 ## コンテナの起動
  * docker container run -d -p 12345:8080 sample-image:0.1
  * curl http://localhost:12345
