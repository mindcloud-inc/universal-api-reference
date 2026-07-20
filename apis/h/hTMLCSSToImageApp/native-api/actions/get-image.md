# Get Image with HTML/CSS to Image app

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/image/:imageId.:format`
- **Base URL:** `https://hcti.io`
- **Official documentation:** [Get Image](https://docs.htmlcsstoimage.com/getting-started/using-the-api/#getting-an-image)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `imageId` | path | `string` | yes |
| `format` | path | `string` | yes |
| `width` | query | `number` | no |
| `height` | query | `number` | no |
| `dpi` | query | `number` | no |
| `dl` | query | `boolean` | no |
| `aspect_ratio` | query | `string` | no |
| `x_origin` | query | `string` | no |
| `y_origin` | query | `string` | no |
| `x_1` | query | `string` | no |
| `x_2` | query | `string` | no |
| `y_1` | query | `string` | no |
| `y_2` | query | `string` | no |
| `crop_width` | query | `string` | no |
| `crop_height` | query | `string` | no |
