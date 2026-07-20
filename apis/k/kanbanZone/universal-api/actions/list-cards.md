# Kanban Zone: List Cards

Retrieves cards from Kanban Zone.

```
GET https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-cards?connectionId=$CONNECTION_ID&limit=25&offset=0&board=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "board": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-cards?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `board` | string | yes | The board public ID. |
| `includeArchived` | boolean | no | Include archived cards in the response. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columns` | string | no | Comma-separated list of column IDs. |
| `daysSinceLastUpdate` | number | no | Filter by cards updated within the last N days. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cards": [
        {}
      ],
      "count": 1,
      "errors": {},
      "hasMore": true,
      "totalAvailable": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cards` | array<object> |  |
| `count` | number |  |
| `errors` | object |  |
| `hasMore` | boolean |  |
| `totalAvailable` | number |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `GET /cards` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cards.md) for the provider-specific parameters and requirements.

