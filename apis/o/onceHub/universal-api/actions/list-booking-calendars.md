# OnceHub: List Booking Calendars



```
GET https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-booking-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-booking-calendars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-booking-calendars?${params}`, {
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
      "durationMinutes": 1,
      "host": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "published": true,
      "subject": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `durationMinutes` | number |  |
| `host` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `published` | boolean |  |
| `subject` | string |  |
| `url` | string |  |

## Native endpoint

Through the native OnceHub API, this operation is `GET /v2/booking-calendars` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-booking-calendars.md) for the provider-specific parameters and requirements.

