# Keywords AI: Create Prompt

Creates a prompt in Keywords AI.

```
POST https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/create-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keywords AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/create-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/create-prompt', {
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
      "prompt_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `prompt_id` | string |  |

## Native endpoint

Through the native Keywords AI API, this operation is `POST /api/prompts/` (base URL `https://api.respan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prompt.md) for the provider-specific parameters and requirements.

