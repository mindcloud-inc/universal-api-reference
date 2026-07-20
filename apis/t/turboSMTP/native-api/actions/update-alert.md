# Update Alert with turboSMTP

Updates an existing alert in turboSMTP.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tools/alerts/{Id}`
- **Base URL:** `https://pro.api.serversmtp.com/api/v2`
- **Official documentation:** [Update Alert](https://serversmtp.com/turbo-api/#/alerts/updateAlert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | path | `number` | yes | Alert identifier. |
| `email` | body | `string` | yes | Email address that receives the alert notification. |
| `percentage` | body | `number` | yes | Usage percentage threshold for the alert. |
