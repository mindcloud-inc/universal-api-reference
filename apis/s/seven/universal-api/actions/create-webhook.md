# Seven: Create Webhook

Creates a new webhook in Seven.

```
POST https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com",
  "eventType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com",
    "eventType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | Destination address of your webhook |
| `headers` | string | no | Custom headers to be sent to the webhook URL. Could contain multiple headers separated by a line break. |
| `eventType` | string | yes | Type of event for which you would like to receive a webhook. Show events all - Sends all events rcs - RCS events and inbound RCS messages sms_mo - New inbound SMS dlr - Status reports of your SMS voice_call - Info about voice calls voice_status - Status updates of voice calls voice_dtmf - Incoming DTMF signals in voice calls tracking - Clicks or views of the Performance Tracking |
| `eventFilter` | string | no | Optional. Sends the webhook only if the filter applies. For example, for different webhooks with different inbound numbers. |
| `requestMethod` | string | no | Request method in which you would like to receive the webhook. POST - Data is sent as an HTTP POST request as application/x-www-form-urlencoded (default) GET - Data is sent as HTTP GET parameter JSON - Data is sent via HTTP POST as JSON payload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "error_message": "string",
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `error_message` | string |  |
| `id` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `POST /hooks` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

