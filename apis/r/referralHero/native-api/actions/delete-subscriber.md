# Delete Subscriber with ReferralHero

Deletes an existing subscriber from ReferralHero.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/:uuid/subscribers/:subscriber_id`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Delete Subscriber](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-subscriber-by-mwr)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes | Subscriber ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
