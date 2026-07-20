# Segmind: Make Fine-Tuned Model Public



```
PUT https://connect.mindcloud.co/v1/universal/segmind/latest/actions/make-fine-tuned-model-public
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Segmind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/make-fine-tuned-model-public" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/segmind/latest/actions/make-fine-tuned-model-public', {
  method: 'PUT',
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
| `message` | string |  |
| `requestId` | string |  |
| `status` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Segmind API, this operation is `PUT /finetune/request/access-update` (base URL `https://api.segmind.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/make-fine-tuned-model-public.md) for the provider-specific parameters and requirements.

