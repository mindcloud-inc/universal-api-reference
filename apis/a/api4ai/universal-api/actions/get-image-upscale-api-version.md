# api4ai: Get Image Upscale API Version

Retrieves the image upscale API version from api4ai.

```
GET https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/get-image-upscale-api-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api4ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/get-image-upscale-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/get-image-upscale-api-version?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `version` | string | Provider API version string. |

## Native endpoint

Through the native api4ai API, this operation is `GET /image-upscale/v1/version` (base URL `https://api4ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-upscale-api-version.md) for the provider-specific parameters and requirements.

