# Resource Guru: List Client Bookings

Retrieves bookings for a client from Resource Guru.

```
GET https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-client-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-client-bookings?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-client-bookings?${params}`, {
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
| `id` | number | yes | Client ID. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": 1,
      "end_at": "string",
      "id": 1,
      "project_id": 1,
      "start_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | number | Client ID. |
| `end_at` | string | Booking end timestamp. |
| `id` | number | Booking ID. |
| `project_id` | number | Project ID. |
| `start_at` | string | Booking start timestamp. |

## Native endpoint

Through the native Resource Guru API, this operation is `GET /clients/:id/bookings` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-bookings.md) for the provider-specific parameters and requirements.

