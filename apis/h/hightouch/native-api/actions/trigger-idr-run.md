# Trigger IDR Run with Hightouch

Triggers an IDR run in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/idr/{graphId}/trigger`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Trigger IDR Run](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `graphId` | path | `string` | yes | The IDR graph ID. |
| `fullRerun` | body | `boolean` | no | Whether to trigger a full IDR rerun. |
