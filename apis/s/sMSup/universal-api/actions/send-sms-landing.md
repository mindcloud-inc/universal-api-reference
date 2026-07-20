# SMSup: Send SMS Landing



```
POST https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/send-sms-landing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/send-sms-landing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ],
  "messages[].from": "MY BRAND",
  "messages[].to": "34666666111",
  "messages[].text": "See your custom page: {LANDING}",
  "landingId": "2749"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/send-sms-landing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}],
    "messages[].from": "MY BRAND",
    "messages[].to": "34666666111",
    "messages[].text": "See your custom page: {LANDING}",
    "landingId": "2749"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[]` | array<object> | yes | Array of messages to send. |
| `messages[].from` | string | yes | Originator address (sender). Example: `MY BRAND`. |
| `messages[].to` | string | yes | Destination mobile number in international format. Example: `34666666111`. |
| `messages[].text` | string | yes | Body of the text message including the {LANDING} tag. Example: `See your custom page: {LANDING}`. |
| `landingId` | number | yes | ID of the landing template created in the account. Example: `2749`. |
| `reportUrl` | string | no | URL where delivery and landing events should be sent. Example: `https://example.com/events`. |
| `fake` | number | no | Set to 1 to simulate submission without cost. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom": "string",
      "errorId": "string",
      "errorMsg": "string",
      "smsId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom` | string |  |
| `errorId` | string |  |
| `errorMsg` | string |  |
| `smsId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native SMSup API, this operation is `POST /api/3.0/sms/send-landing` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-landing.md) for the provider-specific parameters and requirements.

