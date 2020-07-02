+++
title = "Quick Start"
description = "Legacy technologies require you to choose between being real-time or highly-scalable. Event streaming enables you to innovate and win - by being both real-time and highly-scalable."
date = 2020-07-02T08:56:45-04:00
weight = 20
draft = false
bref = "Comprehensive documentation"
toc = true

+++

### Introduction

Download OpenAPI specification: [Download][1]

Confluent: support@confluent.io
URL: https://confluent.io

The Confluent Cloud Metrics API provides actionable operational metrics about your Confluent Cloud deployment. This is a queryable HTTP API in which the user will POST a query written in JSON and get back a time series of metrics specified by the query.

Comprehensive documentation is available on https://docs.confluent.io.

### Authentication

Confluent uses API keys for integrating with Confluent Cloud. Applications must be authorized and authenticated before they can access or manage resources in Confluent Cloud. You can manage your API keys in the Confluent Cloud Dashboard or Confluent Cloud CLI.

An API key is owned by a User or Service Account and inherits the permissions granted to the owner.

Today, you can divide API keys into two classes:

* **Cloud API Keys** - These grant access to the Confluent Cloud Control Plane APIs, such as for Provisioning and Metrics integrations.
* **Cluster API Keys** - These grant access to a single Confluent cluster, such as a specific Kafka or Schema Registry cluster.

**Cloud API Keys are required for the Metrics API**. Cloud API Keys can be created using the [Confluent Cloud CLI](https://docs.confluent.io/current/cloud/cli/).

```bash
ccloud api-key create --resource cloud
```

All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication will also fail.

### api-key

API keys must be sent as an `Authorization: Basic {key}` header with the Key ID as the username and the Key Secret as the password. Remember that HTTP Basic authorization requires you to colon-separate and base64 encode your key. For example, if your API Key ID is `ABCDEFGH123456789` and the corresponding API Key Secret is `XNCIW93I2L1SQPJSJ823K1LS902KLDFMCZPWEO`, then the authorization header will be

```http
Authorization: Basic QUJDREVGR0gxMjM0NTY3ODk6WE5DSVc5M0kyTDFTUVBKU0o4MjNLMUxTOTAyS0xERk1DWlBXRU8=
```

This example header can be generated (using Mac OS X syntax) from the API key with

```bash
$ echo -n "ABCDEFGH123456789:XNCIW93I2L1SQPJSJ823K1LS902KLDFMCZPWEO" | base64
```

| Security Scheme Type      | HTTP  |
| :------------------------ | ----- |
| HTTP Authorization Scheme | basic |

[1]:	blob:https://api.telemetry.confluent.cloud/54e9aaf1-6a07-42b8-9a27-0d27ab5bc469