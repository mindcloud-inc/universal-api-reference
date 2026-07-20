# Create Tracking Source with CallTrackingMetrics

Creates a new tracking source in CallTrackingMetrics.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/sources.json`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [Create Tracking Source](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/ri0maho/update-a-tracking-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the tracking source. |
| `description` | body | `string` | no | An optional description for the tracking source. |
