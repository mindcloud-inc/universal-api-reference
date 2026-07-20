# Placker: Search Cards



```
GET https://connect.mindcloud.co/v1/universal/placker/latest/actions/search-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placker/latest/actions/search-cards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/search-cards?${params}`, {
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
| `title` | string | no | Filter cards by title. Example: `Task 123`. |
| `limit` | number | no | Maximum number of cards to return. Example: `50`. |
| `listId` | number | no | Filter by list ID. Example: `1235`. |
| `boardId` | number | no | Filter by board ID. Example: `1235`. |
| `statuses` | string | no | Filter by card statuses. Example: `OPEN,INPROGRESS`. |
| `members` | string | no | Filter by member IDs. Example: `987,654`. |
| `assignedToMe` | boolean | no | Return cards assigned to the current user. Example: `true`. |
| `includeArchived` | boolean | no | Include archived cards in results. Example: `false`. |
| `attributes` | string | no | Attribute filters. Example: `priority=High`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Placker API returns.

## Native endpoint

Through the native Placker API, this operation is `GET /card` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cards.md) for the provider-specific parameters and requirements.

