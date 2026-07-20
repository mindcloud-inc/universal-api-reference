# List Subscriptions with Beehiiv

Retrieves subscriptions from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/subscriptions`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [List Subscriptions](https://developers.beehiiv.com/api-reference/subscriptions/index)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `expand` | query | `string` | no | Optional list of expandable subscription objects. |
| `status` | query | `string` | no | Optional subscription status filter. |
| `tier` | query | `string` | no | Optional subscription tier filter. |
| `email` | query | `string` | no | Optional exact, case-insensitive email filter. |
| `cursor` | query | `string` | no | Cursor for cursor-based pagination. |
| `creation_date` | query | `string` | no | Filter subscriptions by creation date (YYYY/MM/DD). |
