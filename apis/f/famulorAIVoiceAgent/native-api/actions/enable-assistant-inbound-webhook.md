# Enable Assistant Inbound Webhook with Famulor AI - Voice Agent

Enables inbound webhook notifications for a Famulor assistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/assistants/enable-inbound-webhook`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Enable Assistant Inbound Webhook](https://docs.famulor.io/en/api-reference/assistants/enable-inbound-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | body | `number` | yes | Assistant ID to enable inbound webhooks for. |
| `webhook_url` | body | `string` | yes | Endpoint URL that receives inbound webhook notifications. |
