# Retrieve Subscriber by Email with ReferralHero

Retrieves a subscriber from ReferralHero by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:uuid/subscribers/retrieve_by_email`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Retrieve Subscriber by Email](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#retrieve-subscriber-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Subscriber email. |
| `uuid` | path | `string` | yes | ReferralHero list UUID. |
