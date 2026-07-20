# Segmind: Download Fine-Tuned Model File



```
GET https://connect.mindcloud.co/v1/universal/segmind/latest/actions/download-fine-tuned-model-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Segmind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/download-fine-tuned-model-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/segmind/latest/actions/download-fine-tuned-model-file?${params}`, {
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
      "fileUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | string |  |
| `fileUrl` | string |  |

## Native endpoint

Through the native Segmind API, this operation is `GET /finetune/request/file/download` (base URL `https://api.segmind.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-fine-tuned-model-file.md) for the provider-specific parameters and requirements.

