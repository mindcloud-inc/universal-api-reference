# Guest Show Secret with One-Time Secret

Retrieves guest secret metadata from One-Time Secret by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/guest/secret/:identifier`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Guest Show Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_showsecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Guest secret identifier to retrieve. |
