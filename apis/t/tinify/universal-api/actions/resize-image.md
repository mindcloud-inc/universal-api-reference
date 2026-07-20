# Tinify: Resize Image

Resizes an optimized image in Tinify.

```
PUT https://connect.mindcloud.co/v1/universal/tinify/latest/actions/resize-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/resize-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z",
  "resize.method": "fit"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinify/latest/actions/resize-image', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z",
    "resize.method": "fit"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputId` | string | yes | Tinify output identifier from a prior compression URL. Example: `zr1jp6xybr82ge0s683x67rgwsawjw4z`. |
| `resize.method` | list | yes | Resize method. Scale needs width or height; fit, cover, and thumb need width and height. One of: `0`, `1`, `2`, `3`. Example: `fit`. |
| `resize.width` | number | no | Target width in pixels. Example: `150`. |
| `resize.height` | number | no | Target height in pixels. Example: `100`. |

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
| `type` | string | Raw response object type for the optimized image payload. |

## Native endpoint

Through the native Tinify API, this operation is `POST /output/:outputId` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resize-image.md) for the provider-specific parameters and requirements.

