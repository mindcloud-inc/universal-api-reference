# Ticketmaster: List Venues

Finds venues in Ticketmaster by name and related filters.

```
GET https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-venues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketmaster `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-venues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-venues?${params}`, {
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
      "accessibleSeatingDetail": "string",
      "address": {},
      "city": {},
      "country": {},
      "generalInfo": {},
      "id": "string",
      "images": [
        {}
      ],
      "locale": "string",
      "location": {},
      "name": "Ava Chen",
      "parkingDetail": "string",
      "postalCode": "string",
      "state": {},
      "timezone": "string",
      "type": "string",
      "upcomingEvents": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibleSeatingDetail` | string |  |
| `address` | object |  |
| `city` | object |  |
| `country` | object |  |
| `generalInfo` | object |  |
| `id` | string |  |
| `images` | array<object> |  |
| `locale` | string |  |
| `location` | object |  |
| `name` | string |  |
| `parkingDetail` | string |  |
| `postalCode` | string |  |
| `state` | object |  |
| `timezone` | string |  |
| `type` | string |  |
| `upcomingEvents` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Ticketmaster API, this operation is `GET /discovery/v2/venues` (base URL `https://app.ticketmaster.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-venues.md) for the provider-specific parameters and requirements.

