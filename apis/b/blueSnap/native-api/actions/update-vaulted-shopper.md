# Update Vaulted Shopper with BlueSnap

Updates a vaulted shopper in BlueSnap.

## Endpoint

- **Method:** `PUT`
- **Path:** `/vaulted-shoppers/:vaultedShopperId`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Update Vaulted Shopper](https://developers.bluesnap.com/v8976-JSON/reference/update-vaulted-shopper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vaultedShopperId` | path | `string` | yes | ID of the vaulted shopper to update. |
| `firstName` | body | `string` | no | Updated shopper first name. |
| `lastName` | body | `string` | no | Updated shopper last name. |
| `email` | body | `string` | no | Updated shopper email. |
| `country` | body | `string` | no | Updated shopper country code (ISO-2). |
