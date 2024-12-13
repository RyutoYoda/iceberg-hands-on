FROM bitnami/spark:3.3.2

USER root
RUN mkdir -p /usr/src/dbt_project

# dbt-sparkと依存関係をインストール
RUN pip install dbt-spark[PyHive]

# プロジェクト初期化と必要なファイルコピー
COPY ./dbt_project /usr/src/dbt_project
WORKDIR /usr/src/dbt_project
RUN dbt init iceberg_hands_on
