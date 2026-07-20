# Get Subscription by ID with Beehiiv

Retrieves a subscription from Beehiiv by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/subscriptions/:subscriptionId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Subscription by ID](https://developers.beehiiv.com/api-reference/subscriptions/get-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `subscriptionId` | path | `string` | yes | The prefixed ID of the subscription object. |
| `expand` | query | `string` | no | Optional list of expandable subscription objects. |
