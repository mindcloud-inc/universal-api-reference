# Nvoip: Schedule SMS



```
POST https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/schedule-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/schedule-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "schedulingDate": "string",
  "toNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/schedule-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "schedulingDate": "string",
    "toNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | SMS message to schedule. |
| `schedulingDate` | string | yes | Date and time when the SMS should be sent. |
| `toNumber` | string | yes | Destination number for the scheduled SMS. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mensagem": "string",
      "schedKey": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mensagem` | string | Provider confirmation message. |
| `schedKey` | string | Scheduled SMS identifier. |
| `state` | string | Scheduling result state. |

## Native endpoint

Through the native Nvoip API, this operation is `POST /sched/torpedo` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-sms.md) for the provider-specific parameters and requirements.

