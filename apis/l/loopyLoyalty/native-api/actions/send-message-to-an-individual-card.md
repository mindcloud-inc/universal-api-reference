# Send Message To An Individual Card with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/card/push`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Send Message To An Individual Card](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_sendMessageToIndividualCard)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cardID` | body | `string` | yes |
| `message` | body | `string` | yes |
