# Eventix: Get EventDates

Retrieves event dates from Eventix.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-dates?connectionId=$CONNECTION_ID&type=normal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "normal"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-dates?${params}`, {
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
| `type` | list<string> | yes | How to handle archived EventDates. One of: `0`, `1`, `2`. Default: `normal`. Example: `normal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacity": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "event_id": "string",
      "facebook_event_id": "string",
      "guid": "string",
      "seated": true,
      "seats_event_key": "string",
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | number |  |
| `end` | date |  |
| `event_id` | string |  |
| `facebook_event_id` | string |  |
| `guid` | string |  |
| `seated` | boolean |  |
| `seats_event_key` | string |  |
| `start` | date |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/eventdate/:type` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-dates.md) for the provider-specific parameters and requirements.

