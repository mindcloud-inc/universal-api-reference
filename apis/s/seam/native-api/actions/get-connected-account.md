# Get Connected Account with Seam

Retrieves a connected account from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/connected_accounts/get`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [Get Connected Account](https://docs.seam.co/latest/api/connected_accounts/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connected_account_id` | body | `string` | no | ID of the connected account that you want to get. |
| `email` | body | `string` | no | Email address associated with the connected account that you want to get. |
