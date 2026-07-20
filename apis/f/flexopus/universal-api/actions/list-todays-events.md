# Flexopus: List Today's Events

Retrieves today's events from a Flexopus account.

```
GET https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-todays-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-todays-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-todays-events?${params}`, {
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
| `buildingId` | number | no | Identifier of the building to show events for. |
| `locationId` | number | no | Identifier of the location to show events for. |
| `bookableId` | number | no | Identifier of the bookable to show events for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attendees": [
            {
              "email": "ava@example.com",
              "id": 1,
              "name": "Ava Chen",
              "role": 1,
              "status": 1
            }
          ],
          "bookables": [
            {
              "capacity": 1,
              "id": 1,
              "integration_email": "ava@example.com",
              "name": "Ava Chen",
              "tags": [
                "string"
              ]
            }
          ],
          "classification": 1,
          "description": "string",
          "from": "2026-05-07T12:00:00.000Z",
          "from_timezone": "string",
          "id": 1,
          "name": "Ava Chen",
          "organizer": {
            "name": "Ava Chen"
          },
          "status": 1,
          "to": "2026-05-07T12:00:00.000Z",
          "to_timezone": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].attendees` | array<object> |  |
| `data[].attendees[].email` | string |  |
| `data[].attendees[].id` | number |  |
| `data[].attendees[].name` | string |  |
| `data[].attendees[].role` | number |  |
| `data[].attendees[].status` | number |  |
| `data[].bookables` | array<object> |  |
| `data[].bookables[].capacity` | number |  |
| `data[].bookables[].id` | number |  |
| `data[].bookables[].integration_email` | string |  |
| `data[].bookables[].name` | string |  |
| `data[].bookables[].tags` | array<string> |  |
| `data[].classification` | number |  |
| `data[].description` | string |  |
| `data[].from` | date |  |
| `data[].from_timezone` | string |  |
| `data[].id` | number |  |
| `data[].name` | string |  |
| `data[].organizer` | object |  |
| `data[].organizer.name` | string |  |
| `data[].status` | number |  |
| `data[].to` | date |  |
| `data[].to_timezone` | string |  |

## Native endpoint

Through the native Flexopus API, this operation is `GET /events/today` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-todays-events.md) for the provider-specific parameters and requirements.

