# ThingsBoard: Clear Alarm

Clears an alarm in ThingsBoard.

```
PUT https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/clear-alarm
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/clear-alarm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alarmId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/clear-alarm', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alarmId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alarmId` | string | yes | The ThingsBoard alarm ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledged": true,
      "cleared": true,
      "clearTs": 1,
      "createdTime": 1,
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "originator": {
        "id": "string"
      },
      "severity": "string",
      "status": "string",
      "tenantId": {
        "id": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acknowledged` | boolean |  |
| `cleared` | boolean |  |
| `clearTs` | number |  |
| `createdTime` | number |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `originator.id` | string |  |
| `severity` | string |  |
| `status` | string |  |
| `tenantId.id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `POST /alarm/:alarmId/clear` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-alarm.md) for the provider-specific parameters and requirements.

