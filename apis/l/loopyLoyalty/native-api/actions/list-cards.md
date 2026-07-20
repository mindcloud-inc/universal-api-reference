# List Cards with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/card/cid/:cid`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [List Cards](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listCards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Campaign ID to list cards for. |
| `start` | body | `number` | no | Zero-based row offset for pagination. |
| `length` | body | `number` | no | Number of cards to return. |
| `search` | body | `string` | no | Optional search term applied across customer details. |
