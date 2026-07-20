# Resource Guru: List Resource Bookings

Retrieves bookings for a resource from Resource Guru.

```
GET https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resource-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resource-bookings?connectionId=$CONNECTION_ID&id=900584" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "900584"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resource-bookings?${params}`, {
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
| `id` | number | yes | Resource ID. Default: `900584`. Example: `900584`. |

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

Through the native Resource Guru API, this operation is `GET /resources/:id/bookings` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resource-bookings.md) for the provider-specific parameters and requirements.

