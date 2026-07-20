# DynaPictures: Generate Image

Creates an image from a DynaPictures template.

```
POST https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/generate-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynaPictures `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/generate-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/generate-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Output image format. |
| `metadata` | string | no | Custom metadata to store on the generated image. |
| `params[]` | array<object> | no | Layer parameters to customize during image generation. |
| `params[].backgroundColor` | string | no | Background color of the layer. |
| `params[].borderColor` | string | no | Border color of the layer. |
| `params[].borderRadius` | string | no | Border radius of the layer. |
| `params[].borderWidth` | string | no | Border width of the layer. |
| `params[].chartColor` | string | no | Color of the chart. |
| `params[].chartDataLabels[]` | array<string> | no | Labels shown on the chart axis. |
| `params[].chartDataValues[]` | array<number> | no | Numeric values for the chart data series. |
| `params[].chartLabelColor` | string | no | Color of chart labels. |
| `params[].color` | string | no | Text color for the layer. |
| `params[].imageAlignH` | string | no | Horizontal alignment when imagePosition is align. |
| `params[].imageAlignV` | string | no | Vertical alignment when imagePosition is align. |
| `params[].imageEffect` | string | no | CSS filter-style effect applied to the image. |
| `params[].imagePosition` | string | no | Positioning mode for the image inside its container. |
| `params[].imageUrl` | string | no | Image used for an image layer. |
| `params[].name` | string | no | Name of the layer to customize. |
| `params[].opacity` | number | no | Layer opacity from 0 to 1. |
| `params[].text` | string | no | Text rendered in the layer. |
| `uid` | string | yes | UID of the template to render. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynaPictures API returns.

## Native endpoint

Through the native DynaPictures API, this operation is `POST /designs/:uid` (base URL `https://api.dynapictures.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image.md) for the provider-specific parameters and requirements.

