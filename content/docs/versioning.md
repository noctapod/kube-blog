+++
title = "Versioning"
description = "Confluent APIs ensure stability for your integrations by avoiding the introduction of breaking changes to customers unexpectedly."
date = 2020-07-02T10:48:32-04:00
weight = 22
draft = false
bref = "Confluent APIs ensure stability for your integrations by avoiding the introduction of breaking changes to customers unexpectedly"
toc = false

+++

Confluent APIs ensure stability for your integrations by avoiding the introduction of breaking changes to customers unexpectedly. Confluent will make non-breaking API changes without advance notice. Thus, API clients **must** follow the [Compatibility Policy](https://api.telemetry.confluent.cloud/docs#section/Versioning/Compatibility-Policy) below to ensure your ingtegration remains stable. All APIs follow the API Lifecycle Policy described below, which describes the guarantees API clients can rely on.

Breaking changes will be [widely communicated](https://api.telemetry.confluent.cloud/docs#communication) in advance in accordance with our [Deprecation Policy](https://api.telemetry.confluent.cloud/docs#section/Versioning/Deprecation-Policy). Confluent will provide timelines and a migration path for all API changes, where available. Be sure to subscribe to one or more [communication channels](https://api.telemetry.confluent.cloud/docs#communication) so you don't miss any updates!

One exception to these guidelines is for critical security issues. We will take any necessary actions to mitigate any critical security issue as soon as possible, which may include disabling the vulnerable functionality until a proper solution is available.

Do not consume any Confluent API unless it is documented in the API Reference. All undocumented endpoints should be considered private, subject to change without notice, and not covered by any agreements.

> Note: The "v1" in the URL is not a "major version" in the [Semantic Versioning](https://semver.org/) sense. It is a "generational version" or "meta version", as seen in other APIs like [Github API](https://developer.github.com/v3/versions/) or the [Stripe API](https://stripe.com/docs/api/versioning).