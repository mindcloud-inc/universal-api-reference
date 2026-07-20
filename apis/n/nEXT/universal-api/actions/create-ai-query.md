# NEXT: Create AI Query

Creates a new AI query in NEXT.

```
POST https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/create-ai-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NEXT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/create-ai-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/create-ai-query', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | string | yes | The AI thread that will contain the query. |
| `prompt` | string | yes | The AI query prompt. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NEXT API returns.

## Native endpoint

Through the native NEXT API, this operation is `POST /ai-queries` (base URL `https://rest.eu-west-1.nextapp.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ai-query.md) for the provider-specific parameters and requirements.

