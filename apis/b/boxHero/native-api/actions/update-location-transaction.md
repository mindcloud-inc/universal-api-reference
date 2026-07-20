# Update Location Transaction with BoxHero

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/location-txs/:tx_id`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Update Location Transaction](https://rest.boxhero-app.com/docs/api#/transactions/LocationTxsController_updateTx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_location_id` | body | `number` | no | Source location ID |
| `items[]` | body | `array<object>` | no | Items included in the transaction |
| `memo` | body | `string` | no | Notes for the transaction |
| `partner_id` | body | `number` | no | Partner ID linked to the transaction |
| `revision` | body | `number` | no | Revision number for the transaction update |
| `to_location_id` | body | `number` | no | Destination location ID |
| `tx_id` | path | `number` | yes | Unique identifier for the transaction |
