# LoopedIn: List Roadmaps

Retrieves roadmaps from LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-roadmaps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-roadmaps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-roadmaps?${params}`, {
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
      "columns": [
        {}
      ],
      "id": "string",
      "title": "string",
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
| `columns` | array<object> |  |
| `id` | string |  |
| `title` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /roadmaps` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roadmaps.md) for the provider-specific parameters and requirements.

