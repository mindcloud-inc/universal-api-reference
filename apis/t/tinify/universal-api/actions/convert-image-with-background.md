# Tinify: Convert Image With Background

Converts an optimized image and fills its background in Tinify.

```
PUT https://connect.mindcloud.co/v1/universal/tinify/latest/actions/convert-image-with-background
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/convert-image-with-background" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z",
  "convert.type": "image/jpeg",
  "transform.background": "#000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinify/latest/actions/convert-image-with-background', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z",
    "convert.type": "image/jpeg",
    "transform.background": "#000000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputId` | string | yes | Tinify output identifier from a prior compression URL. Example: `zr1jp6xybr82ge0s683x67rgwsawjw4z`. |
| `convert.type` | list | yes | Target output MIME type for a transparent image that needs a filled background. One of: `0`. Example: `image/jpeg`. |
| `transform.background` | string | yes | Background color, either a hex color such as #000000, white, or black. Example: `#000000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Binary image bytes returned by Tinify. |
| `type` | string | Raw response object type for the converted image payload. |

## Native endpoint

Through the native Tinify API, this operation is `POST /output/:outputId` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-image-with-background.md) for the provider-specific parameters and requirements.

