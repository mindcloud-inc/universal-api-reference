# Add Subscriber with ReferralHero

Creates a new subscriber in ReferralHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:uuid/subscribers`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Add Subscriber](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-coupons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email. |
| `name` | body | `string` | no | Subscriber name. |
| `referrer` | body | `string` | no | Referrer email or referral code. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
