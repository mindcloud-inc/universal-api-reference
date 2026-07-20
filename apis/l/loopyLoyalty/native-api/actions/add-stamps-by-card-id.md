# Add Stamps By Card ID with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/card/cid/:cid/addStamps/:stamps`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Add Stamps By Card ID](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_addStamps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Card ID to add or deduct stamps on. |
| `stamps` | path | `number` | yes | Number of stamps to add. Negative values deduct stamps. |
| `scanLatitude` | body | `number` | no | Optional latitude where the scan took place. |
| `scanLongitude` | body | `number` | no | Optional longitude where the scan took place. |
