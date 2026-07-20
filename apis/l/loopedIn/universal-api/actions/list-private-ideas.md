# LoopedIn: List Private Ideas

Retrieves private ideas from LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-private-ideas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-private-ideas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-private-ideas?${params}`, {
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
      "account": "string",
      "archived": true,
      "category": {},
      "completed": true,
      "created": "string",
      "createdBy": "string",
      "description": "string",
      "effort": 1,
      "followers": [
        {}
      ],
      "id": "string",
      "priority": 1,
      "public": true,
      "title": "string",
      "value": 1,
      "votes": 1,
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `archived` | boolean |  |
| `category` | object |  |
| `completed` | boolean |  |
| `created` | string |  |
| `createdBy` | string |  |
| `description` | string |  |
| `effort` | number |  |
| `followers` | array<object> |  |
| `id` | string |  |
| `priority` | number |  |
| `public` | boolean |  |
| `title` | string |  |
| `value` | number |  |
| `votes` | number |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /ideas` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-private-ideas.md) for the provider-specific parameters and requirements.

