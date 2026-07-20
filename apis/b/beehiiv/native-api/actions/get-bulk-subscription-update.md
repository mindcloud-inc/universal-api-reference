# Get Bulk Subscription Update with Beehiiv

Retrieves a bulk subscription update from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/bulk_subscription_updates/:id`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Bulk Subscription Update](https://developers.beehiiv.com/api-reference/bulk-subscription-updates/show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `id` | path | `string` | yes | The ID of the subscription update object. |
