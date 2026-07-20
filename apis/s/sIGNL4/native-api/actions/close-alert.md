# Close Alert with SIGNL4

Updates an alert as closed in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/alerts/{alertId}/close`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Close Alert](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Id to acknowledge an alert. |
| `descr` | body | `string` | no | — |
| `uid` | body | `string` | yes | — |
