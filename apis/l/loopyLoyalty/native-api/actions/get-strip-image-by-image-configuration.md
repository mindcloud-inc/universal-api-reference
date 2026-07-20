# Get Strip Image By Image Configuration with Loopy Loyalty

## Endpoint

- **Method:** `GET`
- **Path:** `/images`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Get Strip Image By Image Configuration](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getStripImage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | query | `number` | no | Image width. |
| `height` | query | `number` | no | Image height. |
| `padding` | query | `number` | no | Padding. |
| `totalStamps` | query | `number` | no | Total number of stamps. |
| `stampImage` | query | `string` | no | Stamp image template ID. |
| `unstampImage` | query | `string` | no | Unstamped image template ID. |
| `imageType` | query | `string` | no | Image type. |
