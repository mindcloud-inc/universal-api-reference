# Ticketmaster: Get Venue

Retrieves details for a specific venue from Ticketmaster.

```
GET https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-venue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketmaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-venue?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-venue?${params}`, {
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
| `id` | string | yes | The unique identifier for the venue. |

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

Through the native Ticketmaster API, this operation is `GET /discovery/v2/venues/:id` (base URL `https://app.ticketmaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-venue.md) for the provider-specific parameters and requirements.

