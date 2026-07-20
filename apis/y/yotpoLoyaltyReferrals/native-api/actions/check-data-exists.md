# Check Data Exists with Yotpo Loyalty & Referrals

Checks whether user data exists in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/privacy/data/exists`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Check Data Exists](https://loyaltyapi.yotpo.com/reference/data-exists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the user to check. |
