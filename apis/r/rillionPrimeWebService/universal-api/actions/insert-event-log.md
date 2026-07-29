# Rillion Prime Web Service: Insert Event Log

Write an event log entry in Rillion Prime.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-event-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-event-log" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventLogItem": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-event-log', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventLogItem": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventLogItem` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventLogItem.environment` | string | no |  |
| `eventLogItem.eventType` | string | no |  |
| `eventLogItem.source` | string | no |  |
| `eventLogItem.task` | string | no |  |
| `eventLogItem.message` | string | no |  |
| `eventLogItem.description` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-event-log.md) for the provider-specific parameters and requirements.

