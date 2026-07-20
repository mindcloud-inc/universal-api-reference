# Understory: Get Event

Retrieves an event from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The unique identifier of the event. |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity.reserved` | number |  |
| `capacity.total` | number |  |
| `created_at` | date |  |
| `experience_id` | string |  |
| `id` | string |  |
| `sessions[].end_time` | string |  |
| `sessions[].id` | string |  |
| `sessions[].languages[]` | array<string> |  |
| `sessions[].location_id` | string |  |
| `sessions[].start_time` | string |  |
| `sessions[].timezone` | string |  |
| `state` | string |  |
| `updated_at` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/events/{{eventId}}` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

