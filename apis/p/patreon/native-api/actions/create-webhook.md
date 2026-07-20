# Create Webhook with Patreon

Creates a webhook for the current Patreon campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://www.patreon.com/api/oauth2/v2`
- **Official documentation:** [Create Webhook](https://docs.patreon.com#post-api-oauth2-v2-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.triggers[]` | body | `array<string>` | yes | The Patreon webhook events to subscribe to. |
| `data.attributes.uri` | body | `string` | yes | The fully qualified URL that Patreon should call. |
| `data.relationships.campaign.data.id` | body | `string` | yes | The Patreon campaign ID that should trigger the webhook. |
