# List Call Setting Number Assignments with CallTrackingMetrics

Retrieves call setting number assignments from CallTrackingMetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/numbers.json`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [List Call Setting Number Assignments](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/dg3mps1/list-of-numbers-assigned-and-available-to-assign-to-a-call-setting)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_setting_id` | query | `string` | yes | The call setting ID used to filter assigned numbers. |
