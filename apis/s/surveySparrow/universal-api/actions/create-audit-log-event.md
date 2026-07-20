# SurveySparrow: Create Audit Log Event

Creates a subscribed audit log event in SurveySparrow.

```
POST https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-audit-log-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-audit-log-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    {}
  ],
  "httpMethod": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-audit-log-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": [{}],
    "httpMethod": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<object> | yes | Array of event objects with name |
| `httpMethod` | list | yes | The HTTP method for the request |
| `url` | string | yes | URL of audit webhook event |
| `headers` | object | no | Headers object for the webhook request |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `POST /audit_logs/events` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audit-log-event.md) for the provider-specific parameters and requirements.

