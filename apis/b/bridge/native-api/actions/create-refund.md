# Create Refund with Bridge

Creates a refund in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/payment-account/refunds`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create Refund](https://docs.bridgeapi.io/reference/createrefund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment_account_transaction_id` | body | `string` | yes | The id of the payment account transaction you want to refund |
| `amount` | body | `number` | yes | The amount you wish to refund (positive and up to 2 decimals). You can partially refund the payment transaction. |
| `client_reference` | body | `string` | no | An optional reference to link this refund request to your system (100 characters max.) |
| `description` | body | `string` | no | This description is only for an internal purpose and will allow to have information on the Dashboard (140 characters max.) |
