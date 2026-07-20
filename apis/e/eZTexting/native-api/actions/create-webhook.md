# Create Webhook with EZ Texting

Creates a webhook in EZ Texting.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/subscriptions`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [Create Webhook](https://developers.eztexting.com/reference/create_6-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callbackUrl` | body | `string` | yes | Webhook callback URL |
| `insecureSsl` | body | `boolean` | no | Allow insecure SSL for webhook delivery |
| `secret` | body | `string` | no | Webhook signing secret |
| `type` | body | `string` | yes | Webhook type. Allowed values: inbound_text.received, keyword.opt_in, contact.created. |
