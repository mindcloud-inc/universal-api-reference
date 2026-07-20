# Get Static Map with OneMap SG

Retrieves a static map image from OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/staticmap/getStaticImage`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Get Static Map](https://www.onemap.gov.sg/apidocs/staticmap)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layerchosen` | query | `string` | no | The OneMap base layer to render. |
| `latitude` | query | `number` | yes | The map latitude center. |
| `longitude` | query | `number` | yes | The map longitude center. |
| `postal` | query | `string` | no | The postal code to use for the static map request when applicable. |
| `zoom` | query | `number` | no | The zoom level for the static map. |
| `width` | query | `number` | no | The width of the generated image. |
| `height` | query | `number` | no | The height of the generated image. |
| `polygons` | query | `string` | no | Polygon overlays for the static map request. |
| `lines` | query | `string` | no | Line overlays for the static map request. |
| `points` | query | `string` | no | Point overlays for the static map request. |
| `color` | query | `string` | no | The overlay color value. |
| `fillColor` | query | `string` | no | The polygon fill color value. |
