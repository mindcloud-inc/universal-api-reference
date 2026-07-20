# Everhour: Update Time Record

Updates an existing time record in Everhour.

```
PUT https://connect.mindcloud.co/v1/universal/everhour/latest/actions/update-time-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/update-time-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeId": 1,
  "time": 1,
  "date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everhour/latest/actions/update-time-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timeId": 1,
    "time": 1,
    "date": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeId` | number | yes | Everhour time record ID. |
| `time` | number | yes | Duration in seconds. |
| `date` | string | yes | Record date in YYYY-MM-DD format. |
| `task` | string | no | Optional task ID. |
| `user` | number | no | Optional user ID. |
| `comment` | string | no | Optional time record note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "cost": 1,
      "costRate": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "history": [
        {}
      ],
      "id": 1,
      "isLocked": true,
      "lastHistory": {},
      "lockReasons": [
        {}
      ],
      "manualTime": 1,
      "pastDateTime": 1,
      "task": {},
      "time": 1,
      "timerTime": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `cost` | number |  |
| `costRate` | number |  |
| `createdAt` | date |  |
| `date` | date |  |
| `history` | array<object> |  |
| `id` | number |  |
| `isLocked` | boolean |  |
| `lastHistory` | object |  |
| `lockReasons` | array<object> |  |
| `manualTime` | number |  |
| `pastDateTime` | number |  |
| `task` | object |  |
| `time` | number |  |
| `timerTime` | number |  |
| `user` | number |  |

## Native endpoint

Through the native Everhour API, this operation is `PUT /time/:timeId` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-record.md) for the provider-specific parameters and requirements.

