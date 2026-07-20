# Retrieve Transaction with BlueSnap

Retrieves a transaction from BlueSnap.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions/:transactionId`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Retrieve Transaction](https://developers.bluesnap.com/v8976-JSON/reference/retrieve)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | path | `string` | yes | BlueSnap transaction ID to retrieve. |
