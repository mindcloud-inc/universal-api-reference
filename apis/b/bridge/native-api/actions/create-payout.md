# Create Payout with Bridge

Creates a payout in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/payment-account/payouts`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create Payout](https://docs.bridgeapi.io/reference/createpayout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `beneficiary_id` | body | `string` | yes | The id of the payout beneficiary to which you wish to transfer money |
| `amount` | body | `number` | yes | The amount you wish to transfer, positive and up to 2 decimals |
| `label` | body | `string` | yes | This label that will be displayed on your bank account (140 characters max.) |
| `client_reference` | body | `string` | no | An optional reference to link this payout request to your system (100 characters max.) |
