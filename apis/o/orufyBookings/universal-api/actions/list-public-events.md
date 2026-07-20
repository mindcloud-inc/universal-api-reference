# Orufy Bookings: List Public Events



```
GET https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/list-public-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orufy Bookings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/list-public-events?connectionId=$CONNECTION_ID&accessLink=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessLink": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/list-public-events?${params}`, {
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
| `accessLink` | string | yes | The Orufy access link, for example `mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentsDetails": [
        {}
      ],
      "availableDuration": [
        {}
      ],
      "description": "string",
      "duration": 1,
      "location": "string",
      "modes": [
        {}
      ],
      "name": "Ava Chen",
      "slug": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentsDetails` | array<object> |  |
| `availableDuration` | array<object> |  |
| `description` | string |  |
| `duration` | number |  |
| `location` | string |  |
| `modes` | array<object> |  |
| `name` | string |  |
| `slug` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Orufy Bookings API, this operation is `GET /website/events/:accessLink` (base URL `https://bookings.orufy.com/api/v1/bookings`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-events.md) for the provider-specific parameters and requirements.

