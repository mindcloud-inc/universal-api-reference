# Get Alert Notifications with SIGNL4

Retrieves alert notifications from SIGNL4.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/alerts/{alertId}/notifications`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Alert Notifications](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Id of the requested Alert. |
