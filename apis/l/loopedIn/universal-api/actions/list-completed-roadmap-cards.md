# LoopedIn: List Completed Roadmap Cards

Retrieves completed roadmap cards from LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-completed-roadmap-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-completed-roadmap-cards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-completed-roadmap-cards?${params}`, {
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
      "column": {},
      "completed": true,
      "created": "string",
      "id": "string",
      "jira": "string",
      "objective": {},
      "plannedFor": "string",
      "public": true,
      "roadmap": "string",
      "summary": "string",
      "title": "string",
      "updated": "string",
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
| `column` | object |  |
| `completed` | boolean |  |
| `created` | string |  |
| `id` | string |  |
| `jira` | string |  |
| `objective` | object |  |
| `plannedFor` | string |  |
| `public` | boolean |  |
| `roadmap` | string |  |
| `summary` | string |  |
| `title` | string |  |
| `updated` | string |  |
| `votes` | number |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /roadmap-cards` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-completed-roadmap-cards.md) for the provider-specific parameters and requirements.

