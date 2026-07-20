# Get Publication Webhook with Beehiiv

Retrieves a publication webhook from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/webhooks/:endpointId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Publication Webhook](https://developers.beehiiv.com/api-reference/webhooks/show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `endpointId` | path | `string` | yes | The prefixed ID of the webhook object. |
