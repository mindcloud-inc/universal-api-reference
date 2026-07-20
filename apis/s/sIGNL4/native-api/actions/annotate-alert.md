# Annotate Alert with SIGNL4

Creates an annotation for an alert in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/alerts/{alertId}/annotate`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Annotate Alert](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Id of the alert to annotate. |
| `type` | body | `number` | no | <p/><ul><li>0 = None</li><li>1 = Text</li><li>2 = Image</li></ul> |
| `text` | body | `string` | no | — |
| `userId` | body | `string` | no | — |
