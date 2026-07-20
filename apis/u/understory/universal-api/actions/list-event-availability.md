# Understory: List Event Availability

Retrieves event availability for an experience in Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-event-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-event-availability?connectionId=$CONNECTION_ID&limit=25&offset=0&experienceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "experienceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-event-availability?${params}`, {
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
| `experienceId` | string | yes | The unique identifier of the experience to query events for. |
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
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].available` | boolean |  |
| `items[].constraints[].available` | boolean |  |
| `items[].constraints[].cutoff_time` | date |  |
| `items[].constraints[].remaining` | number |  |
| `items[].constraints[].state` | string |  |
| `items[].constraints[].type` | string |  |
| `items[].event_id` | string |  |
| `next` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/event-availabilities` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-event-availability.md) for the provider-specific parameters and requirements.

