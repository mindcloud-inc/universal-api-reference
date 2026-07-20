# Launch27: List Booking Spots

Retrieves available booking spots from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-spots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-spots?connectionId=$CONNECTION_ID&date=string&location_id=1&duration=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "location_id": "1",
  "duration": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-spots?${params}`, {
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
| `date` | string | yes | Start date for booking spot availability in YYYY-MM-DD format. |
| `location_id` | number | yes | Launch27 location ID to search for available spots. |
| `duration` | number | yes | Requested service duration in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "end_time": "string",
      "holiday": true,
      "spots": [
        {}
      ],
      "start_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `end_time` | string |  |
| `holiday` | boolean |  |
| `spots` | array<object> |  |
| `start_time` | string |  |

## Native endpoint

Through the native Launch27 API, this operation is `POST booking/spots` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booking-spots.md) for the provider-specific parameters and requirements.

