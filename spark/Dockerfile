FROM bitnami/spark:3.3.2

USER root
RUN mkdir -p /usr/src/dbt_project

# Icebergとdbt-sparkの依存ライブラリをインストール
RUN pip install dbt-spark[PyHive]
RUN mkdir -p /opt/spark/jars && \
    curl -L -o /opt/spark/jars/iceberg-spark-runtime.jar \
    https://repo1.maven.org/maven2/org/apache/iceberg/iceberg-spark-runtime-3.3_2.12/1.5.0/iceberg-spark-runtime-3.3_2.12-1.5.0.jar
