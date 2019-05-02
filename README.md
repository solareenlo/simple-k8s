# simple-k8s
ローカル環境でKubernetesを動かす.

## Requirement
### Dockerのインストール
先ずはDockerのインストール.

- Macは以下からソフトをダウンロードしてインストールする.  
https://hub.docker.com/editions/community/docker-ce-desktop-mac

- Ubuntuは, 以下を参考にインストールする.  
https://docs.docker.com/install/linux/docker-ce/ubuntu/

### Kubernetesのインストール
1. `kubectl`をインストールする.
  - https://kubernetes.io/docs/tasks/tools/install-kubectl/
  - Kubernetesをコマンドラインで操作するツール.
2. VirtualBoxをインストールする.
  - https://www.virtualbox.org/wiki/Downloads
  - Dockerコンテナを立ち上げる仮想マシン.
3. `minikube`をインストールする.
  - https://kubernetes.io/docs/tasks/tools/install-minikube/
  - 仮想マシン上でシングルノードのKubernetesクラスタを実行するツール.

## Usage
```bash
git clone git@github.com:solareenlo/simple-k8s.git
cd simple-k8s
minikube start # DockerコンテナをVirtualBox上で動かす環境を起動させる.
kubectl apply -f client-deployment.yaml # Deployment機能を使ってコンテナを起動する.
kubectl get pods # 起動しているpod確認
kubectl get deployments # 起動しているdeployment確認
kubectl describe pods # podの詳細確認
```
