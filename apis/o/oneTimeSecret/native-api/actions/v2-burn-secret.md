# Burn Receipt Secret with One-Time Secret

Deletes a secret from One-Time Secret by receipt identifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/receipt/:identifier/burn`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Burn Receipt Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_receipt_burnsecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Receipt identifier for the secret to burn. |
| `continue` | body | `string` | no | Provider confirmation token when required to proceed with burn. |
