# Get UTXO State with Overledger

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/autoexecution/search/utxo/:utxoId`
- **Base URL:** `https://api.overledger.dev`
- **Official documentation:** [Get UTXO State](https://docs.overledger.dev/docs/utxo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `utxoId` | path | `string` | yes | UTXO identifier to inspect, for example transactionHash:index. |
| `location` | body | `object` | yes | Overledger location object with technology and network. |
