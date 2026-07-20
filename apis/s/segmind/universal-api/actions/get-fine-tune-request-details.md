# Segmind: Get Fine-Tune Request Details



```
GET https://connect.mindcloud.co/v1/universal/segmind/latest/actions/get-fine-tune-request-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Segmind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/get-fine-tune-request-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/segmind/latest/actions/get-fine-tune-request-details?${params}`, {
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
      "details": {},
      "message": "string",
      "modelName": "Ava Chen",
      "requestId": "string",
      "status": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object |  |
| `message` | string |  |
| `modelName` | string |  |
| `requestId` | string |  |
| `status` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Segmind API, this operation is `GET /finetune/request/details` (base URL `https://api.segmind.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fine-tune-request-details.md) for the provider-specific parameters and requirements.

