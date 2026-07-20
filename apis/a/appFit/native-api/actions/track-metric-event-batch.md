# Track Metric Event Batch with AppFit

Creates a batch of metric events in AppFit.

## Endpoint

- **Method:** `POST`
- **Path:** `/metric-events/batch`
- **Base URL:** `https://api.appfit.io`
- **Official documentation:** [Track Metric Event Batch](https://www.appfit.io/article/website-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<object>` | yes | Array of AppFit batch event objects. Each item should include eventSource, version, occurredAt, and a payload object with sourceEventId, eventName, origin, optional userId or anonymousId, properties, and systemProperties. |
