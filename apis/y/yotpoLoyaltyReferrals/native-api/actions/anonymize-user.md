# Anonymize User with Yotpo Loyalty & Referrals

Deletes and anonymizes user data in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/privacy/data`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Anonymize User](https://loyaltyapi.yotpo.com/reference/anonymize-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the end-user requesting deletion. |
| `all_stores` | body | `boolean` | no | Delete the user's data across all stores in the organization when true. |
