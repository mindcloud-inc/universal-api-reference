# Create Account with ECAL

Creates a new sub-account in ECAL.

## Endpoint

- **Method:** `POST`
- **Path:** `/account`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Create Account](https://docs.ecal.com/reference/apiv2/account.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's Partner-only account creation payload. |
