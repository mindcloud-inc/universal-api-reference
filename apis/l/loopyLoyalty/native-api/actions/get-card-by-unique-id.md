# Get Card By Unique ID with Loopy Loyalty

## Endpoint

- **Method:** `GET`
- **Path:** `/uniquecard/campaignid/:campaignId/:uniqueIdType/:uniqueIdValue`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Get Card By Unique ID](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getCardByUniqueId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign ID the card belongs to. |
| `uniqueIdType` | path | `string` | yes | Unique ID type: email, phone, or text. |
| `uniqueIdValue` | path | `string` | yes | Value for the chosen unique ID type. |
