# Makeplans: Create Event

Creates a new event in Makeplans.

```
POST https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": 1,
  "serviceId": 1,
  "capacity": 1,
  "startsAt": "2026-05-07T12:00:00.000Z",
  "endsAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": 1,
    "serviceId": 1,
    "capacity": 1,
    "startsAt": "2026-05-07T12:00:00.000Z",
    "endsAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | number | yes | Required Makeplans resource ID. |
| `title` | string | no | Optional event title. |
| `serviceId` | number | yes | Required Makeplans service ID. |
| `capacity` | number | yes | Required event capacity. |
| `startsAt` | date | yes | Event start datetime. |
| `endsAt` | date | yes | Event end datetime. |

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

Through the native Makeplans API, this operation is `POST /events` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

