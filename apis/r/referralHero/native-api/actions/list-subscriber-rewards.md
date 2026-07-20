# List Subscriber Rewards with ReferralHero

Retrieves rewards unlocked by a subscriber in ReferralHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/subscribers/:subscriber_id/rewards`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [List Subscriber Rewards](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#delete-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional reward status filter. |
| `subscriber_id` | path | `string` | yes | Subscriber ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
