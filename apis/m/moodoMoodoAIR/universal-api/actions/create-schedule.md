# Moodo & Moodo AIR: Create Schedule

Creates a new schedule for a Moodo box.

```
POST https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "weekdays": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "weekdays": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `weekdays` | object | yes | Weekday activation map. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "schedule": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `schedule` | object |  |

## Native endpoint

Through the native Moodo & Moodo AIR API, this operation is `POST /schedules` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

