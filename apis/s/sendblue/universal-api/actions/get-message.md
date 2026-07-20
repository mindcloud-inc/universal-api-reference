# Sendblue: Get Message

Retrieves a message from Sendblue by ID.

```
GET https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=13bb119a-d6c4-45b9-b8cd-54a6b8be0965" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "13bb119a-d6c4-45b9-b8cd-54a6b8be0965"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-message?${params}`, {
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
| `messageId` | string | yes | Message handle or ID. Example: `13bb119a-d6c4-45b9-b8cd-54a6b8be0965`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
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
        "service": "string",
        "status": "string",
        "toNumber": "string",
        "wasDowngraded": {}
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.accountEmail` | string |  |
| `data.content` | string |  |
| `data.dateSent` | string |  |
| `data.dateUpdated` | string |  |
| `data.errorCode` | object |  |
| `data.errorDetail` | object |  |
| `data.errorMessage` | object |  |
| `data.errorReason` | object |  |
| `data.fromNumber` | string |  |
| `data.groupDisplayName` | object |  |
| `data.groupId` | string |  |
| `data.isOutbound` | boolean |  |
| `data.mediaUrl` | string |  |
| `data.messageHandle` | string |  |
| `data.messageType` | string |  |
| `data.number` | string |  |
| `data.optedOut` | boolean |  |
| `data.plan` | string |  |
| `data.sendblueNumber` | string |  |
| `data.sendStyle` | string |  |
| `data.service` | string |  |
| `data.status` | string |  |
| `data.toNumber` | string |  |
| `data.wasDowngraded` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `GET /api/v2/messages/:message_id` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

