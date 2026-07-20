# List Level 3 Referrals with ReferralHero

Retrieves level 3 referrals from ReferralHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/subscribers/:subscriber_id/level_3_referrals`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [List Level 3 Referrals](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-level-2-confirmed-referrals-of-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes | Subscriber ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
