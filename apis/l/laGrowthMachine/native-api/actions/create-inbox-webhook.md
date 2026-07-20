# Create Inbox Webhook with LaGrowthMachine

Creates an inbox webhook in LaGrowthMachine.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxWebhooks`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Create Inbox Webhook](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaigns[]` | body | `array<string>` | no | Campaign IDs to scope the webhook to, or `all`. |
| `description` | body | `string` | no | Optional description for the webhook. |
| `name` | body | `string` | yes | Display name of the webhook. |
| `url` | body | `string` | yes | Public URL that receives webhook events. |
