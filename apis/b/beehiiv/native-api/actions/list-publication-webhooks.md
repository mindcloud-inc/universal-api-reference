# List Publication Webhooks with Beehiiv

Retrieves publication webhooks from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/webhooks`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [List Publication Webhooks](https://developers.beehiiv.com/api-reference/webhooks/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `limit` | query | `number` | no | A limit on the number of objects to be returned. |
