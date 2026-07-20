# Track Single Transaction with ReferralHero

Creates a transaction for a subscriber in ReferralHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:uuid/subscribers/add_transactions`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Track Single Transaction](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-rewards-unlocked-by-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Transaction amount. |
| `email` | body | `string` | yes | Subscriber email. |
| `transaction_id` | body | `string` | no | Unique transaction ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
