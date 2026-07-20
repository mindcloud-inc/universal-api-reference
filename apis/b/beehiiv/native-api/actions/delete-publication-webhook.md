# Delete Publication Webhook with Beehiiv

Deletes a publication webhook from Beehiiv.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/publications/:publicationId/webhooks/:endpointId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Delete Publication Webhook](https://developers.beehiiv.com/api-reference/webhooks/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `endpointId` | path | `string` | yes | The prefixed ID of the webhook object. |
