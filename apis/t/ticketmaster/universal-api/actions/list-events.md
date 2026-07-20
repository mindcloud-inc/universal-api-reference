# Ticketmaster: List Events

Finds events in Ticketmaster by location, date, and availability.

```
GET https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketmaster `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-events?${params}`, {
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
| `keyword` | string | no | Keyword to search on. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classifications": [
        {}
      ],
      "dates": {},
      "id": "string",
      "images": [
        {}
      ],
      "info": "string",
      "locale": "string",
      "location": {},
      "name": "Ava Chen",
      "pleaseNote": "string",
      "seatmap": {},
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classifications` | array<object> |  |
| `dates` | object |  |
| `id` | string |  |
| `images` | array<object> |  |
| `info` | string |  |
| `locale` | string |  |
| `location` | object |  |
| `name` | string |  |
| `pleaseNote` | string |  |
| `seatmap` | object |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Ticketmaster API, this operation is `GET /discovery/v2/events` (base URL `https://app.ticketmaster.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

