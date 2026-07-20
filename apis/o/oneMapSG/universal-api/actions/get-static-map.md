# OneMap SG: Get Static Map

Retrieves a static map image from OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-static-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-static-map?connectionId=$CONNECTION_ID&latitude=1.31955&longitude=103.84223" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1.31955",
  "longitude": "103.84223"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-static-map?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `layerChosen` | string | no | The OneMap base layer to render. Default: `default`. Example: `default`. |
| `latitude` | number | yes | The map latitude center. Example: `1.31955`. |
| `longitude` | number | yes | The map longitude center. Example: `103.84223`. |
| `postal` | string | no | The postal code to use for the static map request when applicable. Example: `200640`. |
| `zoom` | number | no | The zoom level for the static map. Default: `17`. Example: `17`. |
| `width` | number | no | The width of the generated image. Default: `400`. Example: `400`. |
| `height` | number | no | The height of the generated image. Default: `512`. Example: `512`. |
| `polygons` | string | no | Polygon overlays for the static map request. Example: `[[1.31955,103.84223],[1.31755,103.84223],[1.31755,103.82223],[1.31755,103.81223],[1.31955,103.84223]]:255,0,0`. |
| `lines` | string | no | Line overlays for the static map request. Example: `[[1.31955,103.84223],[1.3204859,103.8438367]]:177,0,0:3`. |
| `points` | string | no | Point overlays for the static map request. Example: `[1.31955,103.84223]\|[1.3204859,103.8438367]`. |
| `color` | string | no | The overlay color value. Example: `255,0,255`. |
| `fillColor` | string | no | The polygon fill color value. Example: `0,255,0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "image": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image` | string | The static map PNG image returned by OneMap. |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/staticmap/getStaticImage` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-static-map.md) for the provider-specific parameters and requirements.

