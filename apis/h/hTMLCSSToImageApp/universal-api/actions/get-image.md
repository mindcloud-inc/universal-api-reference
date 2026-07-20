# HTML/CSS to Image app: Get Image



```
GET https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-image?connectionId=$CONNECTION_ID&imageId=string&format=png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "string",
  "format": "png"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-image?${params}`, {
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
| `imageId` | string | yes |  |
| `format` | string | yes | Default: `png`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `width` | number | no |  |
| `height` | number | no |  |
| `dpi` | number | no |  |
| `download` | boolean | no |  |
| `aspectRatio` | string | no |  |
| `xOrigin` | string | no |  |
| `yOrigin` | string | no |  |
| `x1` | string | no |  |
| `x2` | string | no |  |
| `y1` | string | no |  |
| `y2` | string | no |  |
| `cropWidth` | string | no |  |
| `cropHeight` | string | no |  |

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
| `data` | array<number> | Binary image bytes returned by the wrapper. |
| `type` | string | Buffer marker for the returned binary image payload. |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `GET /v1/image/:imageId.:format` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image.md) for the provider-specific parameters and requirements.

