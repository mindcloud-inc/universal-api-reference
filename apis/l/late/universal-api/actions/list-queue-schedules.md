# Late: List Queue Schedules



```
GET https://connect.mindcloud.co/v1/universal/late/latest/actions/list-queue-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/late/latest/actions/list-queue-schedules?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/list-queue-schedules?${params}`, {
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
| `profileId` | string | yes |  |
| `queueId` | string | no |  |
| `all` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "exists": true,
      "nextSlots": [
        "2026-05-07T12:00:00.000Z"
      ],
      "queues": [
        {}
      ],
      "schedule": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Returned queue count when `all=true`. |
| `exists` | boolean | Whether a default queue exists for the requested profile. |
| `nextSlots` | array<date> | Upcoming slot timestamps for the returned queue. |
| `queues` | array<object> | All queue schedules when `all=true`. |
| `schedule` | object | Single queue schedule payload when returning one queue. |

## Native endpoint

Through the native Late API, this operation is `GET /queue/slots` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-queue-schedules.md) for the provider-specific parameters and requirements.

