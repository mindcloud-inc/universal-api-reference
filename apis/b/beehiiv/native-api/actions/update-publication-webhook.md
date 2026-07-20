# Update Publication Webhook with Beehiiv

Updates a publication webhook in Beehiiv.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/publications/:publicationId/webhooks/:endpointId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Update Publication Webhook](https://developers.beehiiv.com/api-reference/webhooks/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `endpointId` | path | `string` | yes | The prefixed ID of the webhook object. |
| `event_types[]` | body | `array<string>` | no | The types of events the webhook will receive. |
| `description` | body | `string` | no | A description of the webhook. |
