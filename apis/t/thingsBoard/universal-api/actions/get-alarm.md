# ThingsBoard: Get Alarm

Retrieves an alarm from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-alarm
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-alarm?connectionId=$CONNECTION_ID&alarmId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alarmId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-alarm?${params}`, {
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
| `alarmId` | string | yes | The ThingsBoard alarm ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledged": true,
      "ackTs": 1,
      "cleared": true,
      "clearTs": 1,
      "endTs": 1,
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "originator": {
        "entityType": "string",
        "id": "string"
      },
      "severity": "string",
      "startTs": 1,
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
| `ackTs` | number |  |
| `cleared` | boolean |  |
| `clearTs` | number |  |
| `endTs` | number |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `originator.entityType` | string |  |
| `originator.id` | string |  |
| `severity` | string |  |
| `startTs` | number |  |
| `status` | string |  |
| `tenantId.id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /alarm/:alarmId` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alarm.md) for the provider-specific parameters and requirements.

