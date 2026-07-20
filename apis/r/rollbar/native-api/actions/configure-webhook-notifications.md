# Configure Webhook Notifications with Rollbar

Updates webhook notification settings in Rollbar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/notifications/webhook`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Configure Webhook Notifications](https://docs.rollbar.com/reference/put_api-1-notifications-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | yes | Enable webhook notifications. |
| `url` | body | `string` | yes | Webhook URL. |
