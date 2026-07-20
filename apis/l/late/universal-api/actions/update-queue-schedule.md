# Late: Update Queue Schedule



```
PUT https://connect.mindcloud.co/v1/universal/late/latest/actions/update-queue-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/late/latest/actions/update-queue-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "timezone": "string",
  "slots[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/late/latest/actions/update-queue-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "timezone": "string",
    "slots[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes |  |
| `queueId` | string | no |  |
| `name` | string | no |  |
| `timezone` | string | yes |  |
| `slots[]` | array<object> | yes |  |
| `active` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `setAsDefault` | boolean | no |  |
| `reshuffleExisting` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isNewQueue": true,
      "nextSlots": [
        "2026-05-07T12:00:00.000Z"
      ],
      "reshuffledCount": 1,
      "schedule": {},
      "skippedDailyLimit": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isNewQueue` | boolean | Whether the operation created a new queue instead of updating an existing queue. |
| `nextSlots` | array<date> | Upcoming slot timestamps. |
| `reshuffledCount` | number | Number of queued posts reshuffled. |
| `schedule` | object | Updated queue schedule payload. |
| `skippedDailyLimit` | number | Number of queued posts skipped because of daily limits. |
| `success` | boolean | Whether the queue was updated. |

## Native endpoint

Through the native Late API, this operation is `PUT /queue/slots` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-queue-schedule.md) for the provider-specific parameters and requirements.

