# Send Message To All Cards with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/card/cid/:cid/push`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Send Message To All Cards](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_sendMessageToAllCards)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cid` | path | `string` | yes |
| `message` | body | `string` | yes |
