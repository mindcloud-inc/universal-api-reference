# Create Webhook with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Create Webhook](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callbackUrl` | body | `string` | yes | Webhook callback URL. |
| `title` | body | `string` | yes | Webhook title. |
| `event` | body | `string` | yes | Webhook event: CONNECT_INVITED, ACCEPTS_REQUEST, REPLY_DETECTED, EMAIL_SENT, OPENED, BOUNCED, CLICKED, or UNSUBSCRIBED. |
