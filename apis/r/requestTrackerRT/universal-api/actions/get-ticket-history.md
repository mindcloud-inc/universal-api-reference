# Request Tracker (RT): Get Ticket History

Retrieves a ticket's history from Request Tracker.

```
GET https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-ticket-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Request Tracker (RT) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-ticket-history?connectionId=$CONNECTION_ID&limit=25&offset=0&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-ticket-history?${params}`, {
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
| `ticketId` | string | yes | The numeric RT ticket ID. |

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

Through the native Request Tracker (RT) API, this operation is `GET ticket/:ticketId/history` (base URL `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-ticket-history.md) for the provider-specific parameters and requirements.

