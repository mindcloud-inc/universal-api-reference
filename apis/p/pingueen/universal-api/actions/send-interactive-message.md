# Pingueen: Send Interactive Message



```
POST https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/send-interactive-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingueen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/send-interactive-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client": "string",
  "interactive": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/send-interactive-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client": "string",
    "interactive": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client` | string | yes | Client ID to send the message to. |
| `clientName` | string | no | Client name used when sending by phone number. |
| `clientPhone` | string | no | Client phone number with country prefix. |
| `delay` | string | no | Delay before sending, for example 10m or 2d. |
| `interactive` | object | yes | Interactive message object for list, button, or flow payloads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Message metadata returned by Pingueen, including the message ID. |
| `success` | boolean | Whether the interactive message was accepted successfully. |

## Native endpoint

Through the native Pingueen API, this operation is `POST /messages` (base URL `https://api.pingueen.it/ext/v2/{{credentials.businessname}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-interactive-message.md) for the provider-specific parameters and requirements.

