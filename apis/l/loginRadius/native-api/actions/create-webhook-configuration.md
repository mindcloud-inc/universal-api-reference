# Create Webhook Configuration with LoginRadius

Creates a new webhook configuration in LoginRadius.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/manage/webhooks`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Create Webhook Configuration](https://www.loginradius.com/docs/api/openapi/create-webhook-configuration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Event` | body | `string` | yes | Webhook event to subscribe to. |
| `Name` | body | `string` | yes | Webhook configuration name. |
| `TargetUrl` | body | `string` | yes | Webhook destination URL. |
