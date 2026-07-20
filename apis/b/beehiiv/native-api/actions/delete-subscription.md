# Delete Subscription with Beehiiv

Deletes a subscription from Beehiiv.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/publications/:publicationId/subscriptions/:subscriptionId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Delete Subscription](https://developers.beehiiv.com/api-reference/subscriptions/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `subscriptionId` | path | `string` | yes | The prefixed ID of the subscription object. |
