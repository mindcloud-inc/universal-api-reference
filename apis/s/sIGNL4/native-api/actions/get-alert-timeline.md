# Get Alert Timeline with SIGNL4

Retrieves an alert timeline from SIGNL4.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/alerts/{alertId}/timeline`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Alert Timeline](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Id of the requested Alert. |
| `userId` | query | `string` | no | — |
