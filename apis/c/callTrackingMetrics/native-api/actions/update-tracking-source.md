# Update Tracking Source with CallTrackingMetrics

Updates an existing tracking source in CallTrackingMetrics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/sources/:sourceId.json`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [Update Tracking Source](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/ehkp4cj/create-new-tracking-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceId` | path | `string` | yes | The CallTrackingMetrics tracking source ID. |
| `name` | body | `string` | no | The new tracking source name. |
| `description` | body | `string` | no | An updated description for the tracking source. |
