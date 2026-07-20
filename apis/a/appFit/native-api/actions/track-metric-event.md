# Track Metric Event with AppFit

Creates a metric event in AppFit.

## Endpoint

- **Method:** `POST`
- **Path:** `/metric-events`
- **Base URL:** `https://api.appfit.io`
- **Official documentation:** [Track Metric Event](https://www.appfit.io/article/website-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `occurredAt` | body | `date` | yes | ISO-8601 timestamp for when the metric event occurred. |
| `payload` | body | `object` | yes | AppFit event payload object. Include sourceEventId, eventName, origin, optional userId or anonymousId, properties, and optional systemProperties. |
