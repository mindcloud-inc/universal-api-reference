# Get User Webhook with Zeplin

Retrieves an user webhook from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/me/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get User Webhook](https://docs.zeplin.dev/reference/getuserwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Webhook id |
