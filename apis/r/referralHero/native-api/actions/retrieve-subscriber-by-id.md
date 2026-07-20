# Retrieve Subscriber by ID with ReferralHero

Retrieves a subscriber from ReferralHero by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/subscribers/:subscriber_id`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Retrieve Subscriber by ID](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-all-subscribers-from-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes | Subscriber ID. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
