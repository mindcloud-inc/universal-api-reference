# Segmind: Get Flux Dataset Upload URL



```
GET https://connect.mindcloud.co/v1/universal/segmind/latest/actions/get-flux-dataset-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Segmind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/get-flux-dataset-upload-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/segmind/latest/actions/get-flux-dataset-upload-url?${params}`, {
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
      "expiresAt": "string",
      "fields": {},
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | string |  |
| `fields` | object |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native Segmind API, this operation is `GET /finetune/request/upload/pre-signed-url` (base URL `https://api.segmind.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flux-dataset-upload-url.md) for the provider-specific parameters and requirements.

