# Guest Show Receipt with One-Time Secret

Retrieves a guest receipt from One-Time Secret by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/guest/receipt/:identifier`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Guest Show Receipt](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_showreceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Guest receipt identifier to retrieve. |
