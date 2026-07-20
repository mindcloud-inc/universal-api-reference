# Get Card By ID with Loopy Loyalty

## Endpoint

- **Method:** `GET`
- **Path:** `/card/:cid`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Get Card By ID](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getCardById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Card ID to retrieve. |
| `includeEvents` | query | `boolean` | no | Whether to include card events in the response. |
| `includeRewards` | query | `boolean` | no | Whether to include reward history in the response. |
