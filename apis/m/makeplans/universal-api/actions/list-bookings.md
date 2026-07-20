# Makeplans: List Bookings

Retrieves bookings from Makeplans.

```
GET https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-bookings?${params}`, {
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
| `end` | string | no | Return bookings with booked_to before this datetime. |
| `start` | string | no | Return bookings with booked_from after this datetime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "booked_from": "2026-05-07T12:00:00.000Z",
      "booked_to": "2026-05-07T12:00:00.000Z",
      "count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "notes": "string",
      "person_id": 1,
      "resource_id": 1,
      "service_id": 1,
      "state": "string",
      "status": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `booked_from` | date |  |
| `booked_to` | date |  |
| `count` | number |  |
| `created_at` | date |  |
| `id` | number |  |
| `notes` | string |  |
| `person_id` | number |  |
| `resource_id` | number |  |
| `service_id` | number |  |
| `state` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `GET /bookings` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

