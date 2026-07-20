# Delete User Webhook with Zeplin

Deletes an existing user webhook from Zeplin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/me/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Delete User Webhook](https://docs.zeplin.dev/reference/deleteuserwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Webhook id |
