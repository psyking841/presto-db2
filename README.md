# IBM DB2 connector for Presto [![Build Status](https://travis-ci.org/IBM/presto-db2.svg?branch=master)](https://travis-ci.org/IBM/presto-db2)

This is a plugin for [Presto](https://prestosql.io/) that allow you to use IBM DB2 Jdbc Connection

## Connection Configuration

Create new properties file inside `etc/catalog` dir:

    connector.name=db2
    connection-url=jdbc:db2://ip:port/database
    connection-user=myuser
    connection-password=mypassword
    connection-ssl=true

Or 

    connector.name=db2
    connection-url=jdbc:db2://ip:port/database:sslConnection=true;
    connection-user=myuser
    connection-password=mypassword

**Note, don't forget the colon at the end of the connection-url parameter.**

## Building Presto DB2 JDBC Plugin

    mvn clean install -DskipTests -Dair.check.skip-all=true
