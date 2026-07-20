# Create List with ReferralHero

Creates a new list in ReferralHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://app.referralhero.com/api/v2`
- **Official documentation:** [Create List](https://support.referralhero.com/integrate/rest-api/endpoint-reference-v2#create-a-new-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | List name. |
| `website` | body | `string` | yes | Default referral URL for the new list. |
