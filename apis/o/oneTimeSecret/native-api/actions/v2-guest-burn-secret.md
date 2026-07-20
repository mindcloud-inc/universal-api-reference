# Guest Burn Secret with One-Time Secret

Deletes a guest secret from One-Time Secret by receipt identifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/guest/receipt/:identifier/burn`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Guest Burn Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_burnsecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Guest receipt identifier for the secret to burn. |
| `continue` | body | `string` | no | Provider confirmation token when required to proceed with guest burn. |
