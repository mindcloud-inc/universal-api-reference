# Retrieve Subscriber by MWR with ReferralHero

Finds a subscriber in ReferralHero by MWR.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/subscribers/retrieve_by_mwr`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Retrieve Subscriber by MWR](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-subscriber-by-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mwr` | query | `string` | yes | Referrer referral code. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
