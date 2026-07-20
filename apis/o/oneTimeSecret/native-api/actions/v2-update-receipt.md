# Update Receipt with One-Time Secret

Updates a secret receipt in One-Time Secret.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/receipt/:identifier`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Update Receipt](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_updatereceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Receipt identifier to update. |
| `memo` | body | `string` | no | Optional memo text to store on the receipt. One-Time Secret supports up to 500 characters. Maximum length: 500. |
