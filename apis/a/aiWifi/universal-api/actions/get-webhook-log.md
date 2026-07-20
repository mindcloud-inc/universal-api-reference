# AiWifi: Get webhook log

Retrieves details for a webhook delivery log in AiWifi.

```
GET https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/get-webhook-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AiWifi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/get-webhook-log?connectionId=$CONNECTION_ID&logId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "logId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/get-webhook-log?${params}`, {
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
| `logId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempts": 1,
      "code": 1,
      "endpointUrl": "https://example.com",
      "eventId": "string",
      "eventType": "string",
      "requestSent": {},
      "responseReceived": {},
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempts` | number |  |
| `code` | number |  |
| `endpointUrl` | string |  |
| `eventId` | string |  |
| `eventType` | string |  |
| `requestSent` | object |  |
| `responseReceived` | object |  |
| `status` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native AiWifi API, this operation is `GET /brands/{{brandId}}/webhook-logs/{{logId}}` (base URL `https://api.aiwifi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-log.md) for the provider-specific parameters and requirements.

