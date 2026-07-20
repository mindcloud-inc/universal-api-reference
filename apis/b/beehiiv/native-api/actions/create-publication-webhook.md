# Create Publication Webhook with Beehiiv

Creates a publication webhook in Beehiiv.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/publications/:publicationId/webhooks`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Create Publication Webhook](https://developers.beehiiv.com/api-reference/webhooks/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `url` | body | `string` | yes | The webhook URL to send events to. |
| `event_types[]` | body | `array<string>` | yes | The types of events the webhook will receive. |
| `description` | body | `string` | no | A description of the webhook. |
