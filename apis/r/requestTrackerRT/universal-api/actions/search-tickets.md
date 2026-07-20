# Request Tracker (RT): Search Tickets

Finds tickets in Request Tracker.

```
GET https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/search-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Request Tracker (RT) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/search-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/search-tickets?${params}`, {
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
| `query` | string | yes | TicketSQL query to search RT tickets. |
| `simple` | boolean | no | Set to true to use RT simple search syntax instead of TicketSQL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated RT fields to include in each ticket result. |
| `savedSearch` | string | no | Saved search ID or description to run. Query takes precedence when both are set. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string",
      "Url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `type` | string |  |
| `Url` | string |  |

## Native endpoint

Through the native Request Tracker (RT) API, this operation is `GET tickets` (base URL `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-tickets.md) for the provider-specific parameters and requirements.

