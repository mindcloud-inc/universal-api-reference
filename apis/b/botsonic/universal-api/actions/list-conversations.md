# Botsonic: List Conversations

Retrieves all bot conversations from Botsonic.

```
GET https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-conversations?${params}`, {
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
| `searchQuery` | string | no | Search for conversations matching a query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Conversation type to sort by. |
| `sortOrder` | string | no | Sort direction for conversations. |
| `updatedAfter` | date | no | Filter conversations updated after this ISO 8601 datetime. Example: `2024-01-01T00:00:00Z`. |
| `updatedBefore` | date | no | Filter conversations updated before this ISO 8601 datetime. Example: `2024-12-31T23:59:59Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "page": 1,
      "pages": 1,
      "size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Conversation records. |
| `page` | number | Current page. |
| `pages` | number | Total pages. |
| `size` | number | Page size. |
| `total` | number | Total conversations. |

## Native endpoint

Through the native Botsonic API, this operation is `GET /v1/business/bot-data/conversations/all` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

