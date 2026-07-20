# HelpSpace: List Webhook Logs

Retrieves webhook logs from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-webhook-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-webhook-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-webhook-logs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "properties": {
        "responseBody": "string",
        "statusCode": 1,
        "webhookUrl": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `properties` | object |  |
| `properties.responseBody` | string |  |
| `properties.statusCode` | number |  |
| `properties.webhookUrl` | string |  |

## Native endpoint

Through the native HelpSpace API, this operation is `GET /webhook/logs` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-logs.md) for the provider-specific parameters and requirements.

