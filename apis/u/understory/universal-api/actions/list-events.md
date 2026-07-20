# Understory: List Events

Retrieves events from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-events?${params}`, {
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
| `from` | date | no | Filter events starting from this local date-time. |
| `to` | date | no | Filter events up to this local date-time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "capacity": {
            "reserved": 1,
            "total": 1
          },
          "created_at": "2026-05-07T12:00:00.000Z",
          "experience_id": "string",
          "id": "string",
          "sessions": [
            {
              "end_time": "string",
              "id": "string",
              "languages": [
                [
                  "string"
                ]
              ],
              "location_id": "string",
              "start_time": "string",
              "timezone": "string"
            }
          ],
          "state": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "visibility": "string"
        }
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].capacity.reserved` | number |  |
| `items[].capacity.total` | number |  |
| `items[].created_at` | date |  |
| `items[].experience_id` | string |  |
| `items[].id` | string |  |
| `items[].sessions[].end_time` | string |  |
| `items[].sessions[].id` | string |  |
| `items[].sessions[].languages[]` | array<string> |  |
| `items[].sessions[].location_id` | string |  |
| `items[].sessions[].start_time` | string |  |
| `items[].sessions[].timezone` | string |  |
| `items[].state` | string |  |
| `items[].updated_at` | date |  |
| `items[].visibility` | string |  |
| `next` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/events` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

