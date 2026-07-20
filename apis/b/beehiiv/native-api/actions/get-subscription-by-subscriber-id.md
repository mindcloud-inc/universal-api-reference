# Get Subscription by Subscriber ID with Beehiiv

Retrieves a subscription from Beehiiv by subscriber ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/subscriptions/by_subscriber_id/:subscriberId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Subscription by Subscriber ID](https://developers.beehiiv.com/api-reference/subscriptions/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `subscriberId` | path | `string` | yes | The ID of the subscriber object. |
| `expand` | query | `list<string>` | no | Optional list of expandable objects. Send multiple values as a array. |
