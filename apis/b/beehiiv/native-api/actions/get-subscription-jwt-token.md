# Get Subscription JWT Token with Beehiiv

Generates a subscription JWT token in Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/subscriptions/:subscriptionId/jwt_token`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Subscription JWT Token](https://developers.beehiiv.com/api-reference/subscriptions/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `subscriptionId` | path | `string` | yes | The prefixed ID of the subscription object. |
