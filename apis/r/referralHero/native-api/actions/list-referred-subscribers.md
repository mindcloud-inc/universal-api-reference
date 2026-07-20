# List Referred Subscribers with ReferralHero

Retrieves referred subscribers from ReferralHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/subscribers/:subscriber_id/referred`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [List Referred Subscribers](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#track-bulk-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes | Subscriber ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
