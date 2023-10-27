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

## chapter03のコマンド
### minikube
  * minikube start
  * minikube stop
  * minikube delete
### kind
 * kind create cluster --config kind.yaml --name kindcluster
 * kind get clusters
 * 複数のKubernetesクラスタを利用している場合、kubectlでContextを切り替える。
 * kubectl config use-context kind-kindcluster
 * kind delete cluster -n kindcluseter