# Update Messages in Bulk with ChatDaddy

Performs bulk actions on messages in ChatDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/bulk-action`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Update Messages in Bulk](https://chatdaddy.stoplight.io/docs/openapi/da7f880ef4d31-perform-bulk-actions-on-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Bulk message action to perform. |
| `status` | query | `string` | no | Message status bucket to target for the bulk action. |
