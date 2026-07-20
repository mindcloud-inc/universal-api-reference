# Late: Create Queue Schedule



```
POST https://connect.mindcloud.co/v1/universal/late/latest/actions/create-queue-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/late/latest/actions/create-queue-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "name": "Ava Chen",
  "timezone": "string",
  "slots[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/late/latest/actions/create-queue-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "name": "Ava Chen",
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
| `name` | string | yes |  |
| `timezone` | string | yes |  |
| `slots[]` | array<object> | yes |  |
| `active` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextSlots": [
        "2026-05-07T12:00:00.000Z"
      ],
      "schedule": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextSlots` | array<date> | Upcoming slot timestamps. |
| `schedule` | object | Created queue schedule payload. |
| `success` | boolean | Whether the queue was created. |

## Native endpoint

Through the native Late API, this operation is `POST /queue/slots` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-queue-schedule.md) for the provider-specific parameters and requirements.

