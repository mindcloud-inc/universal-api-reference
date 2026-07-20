# Sendblue: Send Message

Sends a message through Sendblue.

```
POST https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "+584248435662",
  "content": "Stage 3 safe validation",
  "fromNumber": "+16232843671"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "+584248435662",
    "content": "Stage 3 safe validation",
    "fromNumber": "+16232843671"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | string | yes | Recipient phone number in E.164 format. Example: `+584248435662`. |
| `content` | string | yes | Message content. Example: `Stage 3 safe validation`. |
| `fromNumber` | string | yes | Sendblue number to send from. Example: `+16232843671`. |
| `sendStyle` | string | no | Send style. Docs list default, invisible, and '8ball'. Example: `default`. |
| `mediaUrl` | string | no | Remote media URL to attach. Example: `https://httpbin.org/image/png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountEmail": "ava@example.com",
      "content": "string",
      "dateSent": "string",
      "dateUpdated": "string",
      "errorCode": {},
      "errorDetail": {},
      "errorMessage": {},
      "errorReason": {},
      "fromNumber": "string",
      "groupDisplayName": {},
      "groupId": "string",
      "isOutbound": true,
      "mediaUrl": "https://example.com",
      "messageHandle": "string",
      "messageType": "string",
      "number": "string",
      "optedOut": true,
      "plan": "string",
      "sendblueNumber": "string",
      "sendStyle": "string",
      "service": {},
      "status": "string",
      "toNumber": "string",
      "wasDowngraded": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountEmail` | string |  |
| `content` | string |  |
| `dateSent` | string |  |
| `dateUpdated` | string |  |
| `errorCode` | object |  |
| `errorDetail` | object |  |
| `errorMessage` | object |  |
| `errorReason` | object |  |
| `fromNumber` | string |  |
| `groupDisplayName` | object |  |
| `groupId` | string |  |
| `isOutbound` | boolean |  |
| `mediaUrl` | string |  |
| `messageHandle` | string |  |
| `messageType` | string |  |
| `number` | string |  |
| `optedOut` | boolean |  |
| `plan` | string |  |
| `sendblueNumber` | string |  |
| `sendStyle` | string |  |
| `service` | object |  |
| `status` | string |  |
| `toNumber` | string |  |
| `wasDowngraded` | object |  |

## Native endpoint

Through the native Sendblue API, this operation is `POST /api/send-message` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

