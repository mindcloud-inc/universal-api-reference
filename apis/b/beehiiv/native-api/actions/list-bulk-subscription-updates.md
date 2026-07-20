# List Bulk Subscription Updates with Beehiiv

Retrieves bulk subscription updates from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/bulk_subscription_updates`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [List Bulk Subscription Updates](https://developers.beehiiv.com/api-reference/bulk-subscription-updates/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
