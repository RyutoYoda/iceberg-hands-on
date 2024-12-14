FROM apache/spark:3.1.2-hadoop3.2

USER root
RUN apt-get update && apt-get install -y curl && apt-get clean

# Iceberg Spark Runtime jarsダウンロード (バージョンは例として1.3.0)
RUN curl -L https://repo1.maven.org/maven2/org/apache/iceberg/iceberg-spark-runtime-3.1_2.12/1.3.0/iceberg-spark-runtime-3.1_2.12-1.3.0.jar -o /spark/jars/iceberg-spark-runtime.jar

# Minio用のS3コネクタ (hadoop-awsなど)
# 必要であれば追加インストールやJar配置を行ってください

WORKDIR /spark
ENTRYPOINT ["/bin/bash"]
