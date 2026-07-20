# Update Subscriber with ReferralHero

Updates an existing subscriber in ReferralHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:uuid/subscribers/:subscriber_id`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Update Subscriber](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#add-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Updated subscriber email. |
| `name` | body | `string` | no | Updated subscriber name. |
| `subscriber_id` | path | `string` | yes | Subscriber ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
