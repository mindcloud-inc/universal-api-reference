# Update Webhook with Patreon

Updates an existing webhook in Patreon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `https://www.patreon.com/api/oauth2/v2`
- **Official documentation:** [Update Webhook](https://docs.patreon.com#patch-api-oauth2-v2-webhooks-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.paused` | body | `boolean` | no | Patreon accepts false to resume a failed webhook and retry queued events when available. Setting true is rejected by the API. |
| `data.attributes.triggers[]` | body | `array<string>` | no | The Patreon webhook events to subscribe to. |
| `data.attributes.uri` | body | `string` | no | The fully qualified URL that Patreon should call. |
| `webhookId` | path | `string` | yes | The Patreon webhook ID. |
