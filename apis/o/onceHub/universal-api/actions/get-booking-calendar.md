# OnceHub: Get Booking Calendar



```
GET https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-booking-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-booking-calendar?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-booking-calendar?${params}`, {
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
| `id` | string | yes | The OnceHub booking calendar identifier. |

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

Through the native OnceHub API, this operation is `GET /v2/booking-calendars/:id` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-calendar.md) for the provider-specific parameters and requirements.

