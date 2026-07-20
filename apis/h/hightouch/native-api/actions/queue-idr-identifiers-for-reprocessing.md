# Queue IDR Identifiers For Reprocessing with Hightouch

Queues IDR identifiers for reprocessing in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/idr/{graphId}/queue-for-reprocessing`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Queue IDR Identifiers For Reprocessing](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `graphId` | path | `string` | yes | The IDR graph ID. |
| `identifiers[]` | body | `array<object>` | yes | Identifier values to queue for reprocessing, for example [{"identifier":"email","value":"a@b.com"}]. |
| `block` | body | `boolean` | no | Whether to block until reprocessing completes. |
