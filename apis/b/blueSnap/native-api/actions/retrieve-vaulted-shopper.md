# Retrieve Vaulted Shopper with BlueSnap

Retrieves a vaulted shopper from BlueSnap.

## Endpoint

- **Method:** `GET`
- **Path:** `/vaulted-shoppers/:vaultedShopperId`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Retrieve Vaulted Shopper](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-vaulted-shopper)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vaultedShopperId` | path | `string` | yes | BlueSnap vaulted shopper identifier to retrieve. |
