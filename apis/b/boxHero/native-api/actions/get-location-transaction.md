# Get Location Transaction with BoxHero

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/location-txs/:tx_id`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Get Location Transaction](https://rest.boxhero-app.com/docs/api#/transactions/LocationTxsController_getTx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `revision` | query | `number` | no | Specific revision number of the transaction |
| `tx_id` | path | `number` | yes | Unique identifier for the transaction |
