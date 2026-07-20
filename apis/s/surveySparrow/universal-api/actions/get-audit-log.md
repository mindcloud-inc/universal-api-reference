# SurveySparrow: Get Audit Log

Retrieves an audit log from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-audit-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-audit-log?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-audit-log?${params}`, {
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
| `id` | string | yes | ID of the audit log |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actor": {},
      "event": "string",
      "extraData": {},
      "id": "string",
      "ipAddress": "string",
      "message": "string",
      "object": "string",
      "operation": "string",
      "time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actor` | object |  |
| `event` | string |  |
| `extraData` | object |  |
| `id` | string |  |
| `ipAddress` | string |  |
| `message` | string |  |
| `object` | string |  |
| `operation` | string |  |
| `time` | date |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /audit_logs/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-log.md) for the provider-specific parameters and requirements.

