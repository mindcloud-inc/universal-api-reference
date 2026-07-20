# Get Receipt with Loyverse

Retrieves a sales receipt from Loyverse.

## Endpoint

- **Method:** `GET`
- **Path:** `/receipts/:receipt_number`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Get Receipt](https://developer.loyverse.com/docs/#tag/Receipts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `receipt_number` | path | `string` | yes | The unique number of the receipt |
