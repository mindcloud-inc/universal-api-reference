# Private Show Receipt with One-Time Secret

Retrieves a private receipt from One-Time Secret by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/private/:identifier`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Private Show Receipt](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_private_showreceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Private receipt identifier to retrieve. |
