# Create Image Asset with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/imageAsset`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Create Image Asset](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createImageAssets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base64String` | body | `string` | yes | Base64 encoded image string. |
| `type` | body | `string` | yes | The image type. |
| `opacity` | body | `number` | no | The image opacity (0-100). |
