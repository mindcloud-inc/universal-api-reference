# Create Alert Summary with SIGNL4

Creates an alert summary in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/alerts/{alertId}/summarize`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Create Alert Summary](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Id of the alert to create the summary for |
| `language` | query | `string` | no | Language of the requested summary |
