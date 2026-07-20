# Private Burn Secret with One-Time Secret

Deletes a private secret from One-Time Secret by receipt identifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/private/:identifier/burn`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Private Burn Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_private_burnsecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Private receipt identifier for the secret to burn. |
| `continue` | body | `string` | no | Provider confirmation token when required to proceed with private burn. |
