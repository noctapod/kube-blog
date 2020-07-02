+++
title = "Changelog"
description = "This release includes the following changes from the preview release..."
date = 2020-07-02T10:51:26-04:00
weight = 20
draft = false

+++

This release includes the following changes from the preview release:

#### New `format` request attribute

The `/query` request now includes a `format` attribute which controls the result structuring in the response body. See the `/query` endpoint definition for more details.

#### New `/available` endpoint

The new `/available` endpoint allows determining which metrics are available for a set of resources (defined by labels). This endpoint can be used to determine which subset of metrics are currently available for a specific resource (e.g. a Confluent Cloud Kafka cluster).

#### Metric type changes

The `CUMULATIVE_(INT|DOUBLE)` metric type enumeration was changed to `COUNTER_(INT|DOUBLE)`. This was done to better align with OpenTelemetry conventions. In tandem with this change, several metrics that were improperly classified as `GAUGE`s were re-classified as `COUNTER`s.

### Metric name changes

The `/delta` suffix has been removed from the following metrics:

- `io.confluent.kafka.server/received_bytes/delta`
- `io.confluent.kafka.server/sent_bytes/delta`
- `io.confluent.kafka.server/request_count/delta`

**The legacy metric names are deprecated and will stop functioning on 2020-07-01.**