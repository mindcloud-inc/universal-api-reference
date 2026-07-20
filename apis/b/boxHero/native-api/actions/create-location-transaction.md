# Create Location Transaction with BoxHero

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/location-txs`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Create Location Transaction](https://rest.boxhero-app.com/docs/api#/transactions/LocationTxsController_createTx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_location_id` | body | `number` | no | Source location ID |
| `items[]` | body | `array<object>` | yes | Items included in the transaction |
| `memo` | body | `string` | no | Notes for the transaction |
| `partner_id` | body | `number` | no | Partner ID linked to the transaction |
| `to_location_id` | body | `number` | yes | Destination location ID |
| `tx_time` | body | `date` | no | Transaction timestamp |
| `type` | body | `string` | yes | Transaction type |
