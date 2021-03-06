## アプリ概要
MLOps学習の一環として、糖尿病診断アプリを作成しました。各測定データを入力することで、その患者が糖尿病か否かの二値分類予測を行います。  以前参加したSIGNATEのコンペ：[【第8回_Beginner限定コンペ】診断データを使った糖尿病発症予測](https://signate.jp/competitions/414)を題材とさせていただいております。

URL：http://mlops-diabetes-diagnosis-alb-1799143370.ap-northeast-1.elb.amazonaws.com:5050/

Microsoft社の定義するMLOpsの3つ重要概念を参考に、以下を考慮しました。
- モデルのより迅速な実験と開発 → 機械学習向けPipelineライブラリgorkartによるワークフロー管理
- 実稼働環境へのモデルのより迅速なデプロイ → GitHub Actionsを使用したCI/CDパイプラインの構築
- 品質保証 → 各特徴量や正解ラベルの分布、評価指標のモニタリング機能を実装

### アプリ概要とワークフロー

![MLOpsAppワークフロー](https://user-images.githubusercontent.com/62184606/154518012-83d86db5-a05f-48f5-a4eb-408859dbf6cd.png)


## 使用技術
- Python 3.7.4
  - Dash / gokart / scikit-learn / Pandas / SqlAlchemy / PyMySQL
- MySQL 5.7
- Docker / Docker-compose
- GitHub Actions
- AWS
  - ECS(Fargate) / ECR / RDS / EC2 / ELB / SSM

## インフラ構成

![aws_infla](https://user-images.githubusercontent.com/62184606/154516808-92c49f65-8ee4-4489-ac18-03bee88a8f73.png)
