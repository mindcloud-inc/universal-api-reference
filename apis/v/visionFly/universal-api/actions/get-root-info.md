# VisionFly: Get Root Info

Retrieves API details from VisionFly.

```
GET https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/get-root-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VisionFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/get-root-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/get-root-info?${params}`, {
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
      "docs_url": "https://example.com",
      "name": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs_url` | string | Provider documentation URL. |
| `name` | string | API name. |
| `version` | string | API version. |

## Native endpoint

Through the native VisionFly API, this operation is `GET /` (base URL `https://api.visionfly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-root-info.md) for the provider-specific parameters and requirements.

