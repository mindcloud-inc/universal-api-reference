# Socialbu: Run AI Tool

Runs an AI tool in SocialBu.

```
POST https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/run-ai-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/run-ai-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/run-ai-tool', {
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
      "content": "string",
      "data": {},
      "result": "string",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `data` | object |  |
| `result` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `POST /ai/tools/{slug}` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-ai-tool.md) for the provider-specific parameters and requirements.

