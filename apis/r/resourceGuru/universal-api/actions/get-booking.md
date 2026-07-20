# Resource Guru: Get Booking

Retrieves a booking from Resource Guru.

```
GET https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/get-booking?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/get-booking?${params}`, {
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
| `id` | number | yes | Booking ID. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end_at": "string",
      "id": 1,
      "project_id": 1,
      "resource_id": 1,
      "start_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end_at` | string | Booking end timestamp. |
| `id` | number | Booking ID. |
| `project_id` | number | Project ID. |
| `resource_id` | number | Resource ID. |
| `start_at` | string | Booking start timestamp. |

## Native endpoint

Through the native Resource Guru API, this operation is `GET /bookings/:id` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

