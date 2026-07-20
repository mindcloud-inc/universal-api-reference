# Chatrace: Create Opportunity Comment

Creates a new comment on a Chatrace opportunity.

```
POST https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/create-opportunity-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/create-opportunity-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/create-opportunity-comment', {
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
      "created_at": "string",
      "created_by": 1,
      "data": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `created_by` | number |  |
| `data` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Chatrace API, this operation is `POST /pipelines/:pipeline_id/opportunities/:opportunity_id/comments` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity-comment.md) for the provider-specific parameters and requirements.

