# Sendblue: Send Group Message

Sends a group message through Sendblue.

```
POST https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-group-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-group-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-group-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | Message text content. |
| `fromNumber` | string | yes | The Sendblue phone number to send from in E.164 format. |
| `groupId` | string | no | The identifier for an existing group. |
| `mediaUrl` | string | no | A media file URL to send with the message. |
| `numbers[]` | array<string> | no | Recipient phone numbers in E.164 format. Accepts multiple values as an array. |

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
      "number": [
        "string"
      ],
      "optedOut": true,
      "plan": "string",
      "sendblueNumber": "string",
      "sendStyle": "string",
      "service": {},
      "status": "string",
      "toNumber": [
        "string"
      ],
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
| `number[]` | string |  |
| `optedOut` | boolean |  |
| `plan` | string |  |
| `sendblueNumber` | string |  |
| `sendStyle` | string |  |
| `service` | object |  |
| `status` | string |  |
| `toNumber[]` | string |  |
| `wasDowngraded` | object |  |

## Native endpoint

Through the native Sendblue API, this operation is `POST /api/send-group-message` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-group-message.md) for the provider-specific parameters and requirements.

