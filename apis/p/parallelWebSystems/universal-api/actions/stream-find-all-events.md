# Parallel Web Systems: Stream FindAll Events



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-find-all-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-find-all-events?connectionId=$CONNECTION_ID&findallId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "findallId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/stream-find-all-events?${params}`, {
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
| `findallId` | string | yes | The Parallel FindAll run ID. |
| `lastEventId` | string | no | Resume streaming after this event ID. |
| `timeout` | number | no | Long-poll timeout in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "candidate_id": "string",
        "match_status": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "event_id": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.candidate_id` | string | Candidate identifier. |
| `data.match_status` | string | Candidate match status. |
| `data.name` | string | Candidate name. |
| `data.url` | string | Candidate URL. |
| `event_id` | string | Event identifier. |
| `timestamp` | date | Event timestamp. |
| `type` | string | Event type. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `GET /v1beta/findall/runs/:findall_id/events` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-find-all-events.md) for the provider-specific parameters and requirements.

