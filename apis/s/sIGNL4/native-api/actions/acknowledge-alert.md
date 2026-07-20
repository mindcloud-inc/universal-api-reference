# Acknowledge Alert with SIGNL4

Updates an alert as acknowledged in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/alerts/{alertId}/acknowledge`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Acknowledge Alert](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Id to acknowledge an alert. |
| `descr` | body | `string` | no | — |
| `uid` | body | `string` | yes | — |
