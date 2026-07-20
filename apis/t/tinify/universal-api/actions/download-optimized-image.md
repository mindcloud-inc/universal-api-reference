# Tinify: Download Optimized Image

Downloads an optimized image from Tinify.

```
GET https://connect.mindcloud.co/v1/universal/tinify/latest/actions/download-optimized-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/download-optimized-image?connectionId=$CONNECTION_ID&outputId=zr1jp6xybr82ge0s683x67rgwsawjw4z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "outputId": "zr1jp6xybr82ge0s683x67rgwsawjw4z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinify/latest/actions/download-optimized-image?${params}`, {
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
| `outputId` | string | yes | Tinify output identifier from a prior compression URL. Example: `zr1jp6xybr82ge0s683x67rgwsawjw4z`. |

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
| `type` | string | Raw response object type for the downloaded optimized image. |

## Native endpoint

Through the native Tinify API, this operation is `GET /output/:outputId` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-optimized-image.md) for the provider-specific parameters and requirements.

