# Makeplans: List Events

Retrieves events from Makeplans.

```
GET https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-events?${params}`, {
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
| `end` | string | no | Return events with ends_at before this datetime. |
| `start` | string | no | Return events with starts_at after this datetime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": 1,
      "capacity": 1,
      "description": "string",
      "ends_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "nr_of_attendances": 1,
      "published": true,
      "resource_id": 1,
      "service_id": 1,
      "starts_at": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | number |  |
| `capacity` | number |  |
| `description` | string |  |
| `ends_at` | date |  |
| `id` | number |  |
| `nr_of_attendances` | number |  |
| `published` | boolean |  |
| `resource_id` | number |  |
| `service_id` | number |  |
| `starts_at` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Makeplans API, this operation is `GET /events` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

