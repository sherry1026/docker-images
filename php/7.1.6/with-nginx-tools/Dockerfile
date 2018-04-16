FROM registry.cn-hangzhou.aliyuncs.com/mustanggu/docker-images:7.1.6-alpine-opcache-debug
RUN apk update && apk add libaio
COPY instantclient_12_2.zip ./
RUN unzip instantclient_12_2.zip && \
    mv instantclient_12_2/ /usr/lib/ && \
    rm instantclient_12_2.zip && \
    ln /usr/lib/instantclient_12_2/libclntsh.so.12.1 /usr/lib/libclntsh.so && \
    ln /usr/lib/instantclient_12_2/libocci.so.12.1 /usr/lib/libocci.so && \
    ln /usr/lib/instantclient_12_2/libociei.so /usr/lib/libociei.so && \
    ln /usr/lib/instantclient_12_2/libnnz12.so /usr/lib/libnnz12.so
ENV ORACLE_BASE /usr/lib/instantclient_12_2
ENV LD_LIBRARY_PATH /usr/lib/instantclient_12_2
ENV TNS_ADMIN /usr/lib/instantclient_12_2
ENV ORACLE_HOME /usr/lib/instantclient_12_2
RUN pecl install oci8