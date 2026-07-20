# NeroBot AI: Redraw Image

Creates an image redraw task in NeroBot AI.

```
POST https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/redraw-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeroBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/redraw-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/redraw-image', {
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
      "result": {
        "output": "string"
      },
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.output` | string |  |
| `status` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native NeroBot AI API, this operation is `POST /biz/api/task` (base URL `https://api.nero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redraw-image.md) for the provider-specific parameters and requirements.

