# Get Analytics Events with Typesense

Retrieves recent analytics events from Typesense.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/events`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Get Analytics Events](https://typesense.org/docs/30.0/api/analytics-query-suggestions.html#send-events-via-api)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Analytics event name. |
