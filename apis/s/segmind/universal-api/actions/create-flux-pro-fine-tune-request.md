# Segmind: Create Flux Pro Fine-Tune Request



```
POST https://connect.mindcloud.co/v1/universal/segmind/latest/actions/create-flux-pro-fine-tune-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Segmind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/create-flux-pro-fine-tune-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/segmind/latest/actions/create-flux-pro-fine-tune-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "modelName": "Ava Chen",
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `modelName` | string |  |
| `requestId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Segmind API, this operation is `POST /finetune/request/submit` (base URL `https://api.segmind.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-flux-pro-fine-tune-request.md) for the provider-specific parameters and requirements.

