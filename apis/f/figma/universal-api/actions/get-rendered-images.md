# Figma: Get Rendered Images

Retrieves rendered images from a Figma file.

```
GET https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-rendered-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-rendered-images?connectionId=$CONNECTION_ID&key=string&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-rendered-images?${params}`, {
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
| `key` | string | yes | Key of the file to render images from. |
| `ids` | string | yes | Comma-separated node IDs to render. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | string | no | Version ID to render from. |
| `scale` | number | no | Scale factor for rendered images. |
| `format` | string | no | Image format to render (jpg, png, svg, pdf). |
| `svgOutlineText` | boolean | no | Whether to outline text in SVG output. |
| `svgIncludeId` | boolean | no | Whether to include IDs in SVG output. |
| `svgIncludeNodeId` | boolean | no | Whether to include node IDs in SVG output. |
| `svgSimplifyStroke` | boolean | no | Whether to simplify stroke geometry in SVG output. |
| `contentsOnly` | boolean | no | Whether to render only node contents without effects. |
| `useAbsoluteBounds` | boolean | no | Whether to use absolute bounds for rendering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "err": "string",
      "images": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `err` | string |  |
| `images` | object |  |

## Native endpoint

Through the native Figma API, this operation is `GET /images/:key` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rendered-images.md) for the provider-specific parameters and requirements.

