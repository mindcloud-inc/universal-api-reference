# Parsio: Update Webhook



```
PUT https://connect.mindcloud.co/v1/universal/parsio/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parsio/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | string | yes | Webhook ID. |
| `url` | string | no | Destination webhook URL. |
| `event` | string | no | Trigger event. |
| `enabled` | boolean | no | Whether the webhook is enabled. |
| `tableId` | string | no | Table ID for table.parsed events. Default: `default`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errFields": {},
      "errMsg": "string",
      "isError": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errFields` | object | Provider error field details. |
| `errMsg` | string | Provider error message. |
| `isError` | boolean | Whether the update failed. |

## Native endpoint

Through the native Parsio API, this operation is `POST /webhooks` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

