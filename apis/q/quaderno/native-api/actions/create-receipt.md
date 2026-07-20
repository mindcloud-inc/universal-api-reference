# Create Receipt with Quaderno

Creates a paid receipt in Quaderno.

## Endpoint

- **Method:** `POST`
- **Path:** `/receipts`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Create Receipt](https://developers.quaderno.io/api/#tag/Receipts/operation/createReceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | yes | Existing contact object. |
| `currency` | body | `string` | no | Receipt currency code. |
| `items[]` | body | `array<object>` | yes | Receipt line items array. |
| `payments[]` | body | `array<object>` | yes | Receipt payments array. |
