# Retrieve Card Info with BlueSnap

Retrieves card information from BlueSnap.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/credit-card-info-resolver`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Retrieve Card Info](https://developers.bluesnap.com/v8976-Tools/reference/retrieve-card-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardNumber` | body | `string` | yes | Card BIN or card number to resolve metadata. |
