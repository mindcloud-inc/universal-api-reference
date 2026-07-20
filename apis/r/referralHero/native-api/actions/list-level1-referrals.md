# List Level 1 Referrals with ReferralHero

Retrieves level 1 referrals from ReferralHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/subscribers/:subscriber_id/level_1_referrals`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [List Level 1 Referrals](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-level-2-referrals-pending-unconfirmed-confirmed-of-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes | Subscriber ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
