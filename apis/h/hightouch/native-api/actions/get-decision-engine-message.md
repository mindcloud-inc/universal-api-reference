# Get Decision Engine Message with Hightouch

Retrieves a decision engine message from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/decision-engine/flow/{flowId}/messages/{messageId}`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Get Decision Engine Message](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `string` | yes | The Decision Engine flow ID. |
| `messageId` | path | `string` | yes | The Decision Engine message ID. |
