# Makeplans: Update Event

Updates an existing event in Makeplans.

```
PUT https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `capacity` | number | no | Event capacity. |
| `eventId` | number | yes | The Makeplans event ID. |
| `title` | string | no | Event title. |

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

Through the native Makeplans API, this operation is `PUT /events/:eventId` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

