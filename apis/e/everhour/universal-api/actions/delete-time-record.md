# Everhour: Delete Time Record

Deletes an existing time record from Everhour.

```
DELETE https://connect.mindcloud.co/v1/universal/everhour/latest/actions/delete-time-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/delete-time-record?connectionId=$CONNECTION_ID&timeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/delete-time-record?${params}`, {
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
| `timeId` | number | yes | Everhour time record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
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

Through the native Everhour API, this operation is `DELETE /time/:timeId` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-record.md) for the provider-specific parameters and requirements.

