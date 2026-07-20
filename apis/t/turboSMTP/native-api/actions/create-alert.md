# Create Alert with turboSMTP

Creates a new alert in turboSMTP.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/alerts`
- **Base URL:** `https://pro.api.serversmtp.com/api/v2`
- **Official documentation:** [Create Alert](https://serversmtp.com/turbo-api/#/alerts/createAlert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address that receives the alert notification. |
| `percentage` | body | `number` | yes | Usage percentage threshold for the alert. |
