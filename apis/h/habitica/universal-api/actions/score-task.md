# Habitica: Score Task

Scores a task in Habitica.

```
PUT https://connect.mindcloud.co/v1/universal/habitica/latest/actions/score-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/score-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "direction": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/habitica/latest/actions/score-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "direction": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The Habitica task ID. |
| `direction` | string | yes | Score direction, usually up or down. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appVersion": "string",
      "buffs": {},
      "class": "string",
      "delta": 1,
      "exp": 1,
      "gp": 1,
      "hp": 1,
      "lvl": 1,
      "mp": 1,
      "notifications": [
        {}
      ],
      "Tmp": {},
      "training": {},
      "userV": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appVersion` | string |  |
| `buffs` | object |  |
| `class` | string |  |
| `delta` | number |  |
| `exp` | number |  |
| `gp` | number |  |
| `hp` | number |  |
| `lvl` | number |  |
| `mp` | number |  |
| `notifications` | array<object> |  |
| `Tmp` | object |  |
| `training` | object |  |
| `userV` | number |  |

## Native endpoint

Through the native Habitica API, this operation is `POST /tasks/:taskId/score/:direction` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/score-task.md) for the provider-specific parameters and requirements.

