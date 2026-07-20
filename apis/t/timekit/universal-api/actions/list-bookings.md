# Timekit: List Bookings

Lists all existing bookings in Timekit.

```
GET https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-bookings?${params}`, {
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
| `end` | string | no |  |
| `include` | string | no |  |
| `limit` | number | no |  |
| `orderBy` | string | no |  |
| `page` | number | no |  |
| `search` | string | no |  |
| `sortedBy` | string | no |  |
| `start` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "graph": "string",
      "id": "string",
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean |  |
| `created_at` | date |  |
| `graph` | string |  |
| `id` | string |  |
| `state` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Timekit API, this operation is `GET /bookings` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

