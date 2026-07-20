# Add Subscription Tag with Beehiiv

Adds tags to a subscription in Beehiiv.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/publications/:publicationId/subscriptions/:subscriptionId/tags`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Add Subscription Tag](https://developers.beehiiv.com/api-reference/subscription-tags/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `subscriptionId` | path | `string` | yes | The prefixed ID of the subscription object. |
| `tags[]` | body | `array<string>` | yes | Tags that can be used to group subscribers. |
