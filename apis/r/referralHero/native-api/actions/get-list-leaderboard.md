# Get List Leaderboard with ReferralHero

Retrieves a list leaderboard from ReferralHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/leaderboard`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Get List Leaderboard](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#get-list-leaderboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Number of subscribers to return in the leaderboard (10-100). |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
