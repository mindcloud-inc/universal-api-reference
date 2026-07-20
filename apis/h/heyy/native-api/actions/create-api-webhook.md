# Create API Webhook with Heyy

Creates a new API webhook in Heyy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_webhooks`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Create API Webhook](https://docs.heyy.io/api-reference/create-api-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | body | `string` | no | The channel ID for the webhook. |
| `tenantId` | body | `string` | yes | The Heyy tenant ID. |
| `type` | body | `string` | yes | The webhook event type. |
| `url` | body | `string` | yes | The webhook destination URL. |
