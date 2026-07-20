# Chatrace: List Opportunity Comments

Retrieves comments from a Chatrace opportunity.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-opportunity-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-opportunity-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-opportunity-comments?${params}`, {
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

Through the native Chatrace API, this operation is `GET /pipelines/:pipeline_id/opportunities/:opportunity_id/comments` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opportunity-comments.md) for the provider-specific parameters and requirements.

