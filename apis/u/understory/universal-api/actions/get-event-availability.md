# Understory: Get Event Availability

Retrieves event availability from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-event-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-event-availability?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-event-availability?${params}`, {
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
      "available": true,
      "constraints": [
        {
          "available": true,
          "cutoff_time": "2026-05-07T12:00:00.000Z",
          "remaining": 1,
          "state": "string",
          "type": "string"
        }
      ],
      "event_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |
| `constraints[].available` | boolean |  |
| `constraints[].cutoff_time` | date |  |
| `constraints[].remaining` | number |  |
| `constraints[].state` | string |  |
| `constraints[].type` | string |  |
| `event_id` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/event-availabilities/{{eventId}}` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-availability.md) for the provider-specific parameters and requirements.

