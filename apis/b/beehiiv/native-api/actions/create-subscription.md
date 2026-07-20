# Create Subscription with Beehiiv

Creates a subscription in Beehiiv.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/publications/:publicationId/subscriptions`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Create Subscription](https://developers.beehiiv.com/api-reference/subscriptions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `email` | body | `string` | yes | Email address for the new subscription. |
