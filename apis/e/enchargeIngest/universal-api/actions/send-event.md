# Encharge Ingest: Send Event



```
POST https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/send-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encharge Ingest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/send-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "user": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/send-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "user": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the event to record in Encharge. |
| `user` | object | yes | JSON object for the current user. Include at least `email` or `userId`. |
| `properties` | object | no | JSON object with event properties. |
| `sourceIp` | string | no | End-user IP address, if available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Encharge Ingest API, this operation is `POST /` (base URL `https://ingest.encharge.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-event.md) for the provider-specific parameters and requirements.

