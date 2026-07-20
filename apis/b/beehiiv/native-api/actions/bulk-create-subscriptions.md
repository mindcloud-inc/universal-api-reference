# Bulk Create Subscriptions with Beehiiv

Creates subscriptions in bulk in Beehiiv.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/publications/:publicationId/bulk_subscriptions`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Bulk Create Subscriptions](https://developers.beehiiv.com/api-reference/bulk-subscriptions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `subscriptions[]` | body | `array<object>` | yes | Subscriptions payload array. |
