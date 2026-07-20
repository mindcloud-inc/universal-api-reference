# Get Alert with SIGNL4

Retrieves an alert from SIGNL4 by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/alerts/{alertId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Alert](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Id of the requested Alert. |
| `userId` | query | `string` | no | — |
