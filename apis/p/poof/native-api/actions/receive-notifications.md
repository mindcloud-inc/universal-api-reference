# Receive Notifications with Poof

Creates a new webhook in Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.poof.io/api/v1/create_webhook`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Receive Notifications](https://docs.poof.io/reference/notifications-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook callback URL. |
