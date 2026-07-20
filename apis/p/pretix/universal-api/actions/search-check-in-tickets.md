# pretix: Search Check In Tickets

Searches check-in tickets in pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/search-check-in-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/search-check-in-tickets?connectionId=$CONNECTION_ID&organizer=string&list=string&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string",
  "list": "string",
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/search-check-in-tickets?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. |
| `list` | string | yes | Check-in list ID to search within. |
| `search` | string | yes | Ticket, attendee, or order search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "attendeeEmail": "ava@example.com",
      "attendeeName": "Ava Chen",
      "checkins": [
        {}
      ],
      "id": 1,
      "item": 1,
      "order": "string",
      "positionid": 1,
      "price": "string",
      "variation": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers[]` | object |  |
| `attendeeEmail` | string |  |
| `attendeeName` | string |  |
| `checkins[]` | object |  |
| `id` | number |  |
| `item` | number |  |
| `order` | string |  |
| `positionid` | number |  |
| `price` | string |  |
| `variation` | number |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/checkinrpc/search/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-check-in-tickets.md) for the provider-specific parameters and requirements.

