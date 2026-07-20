# List Rewards for All Subscribers with ReferralHero

Retrieves all subscriber rewards for a list in ReferralHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/rewards`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [List Rewards for All Subscribers](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-rewards-for-all-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional reward status filter. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
