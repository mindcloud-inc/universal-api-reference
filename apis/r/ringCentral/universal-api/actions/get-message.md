# RingCentral: Get Message

Retrieves a message from a RingCentral extension.

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-message?connectionId=$CONNECTION_ID&accountId=string&extensionId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "extensionId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-message?${params}`, {
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
| `accountId` | string | yes |  |
| `extensionId` | string | yes |  |
| `messageId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {
          "contentType": "string",
          "id": 1,
          "type": "string",
          "uri": "string"
        }
      ],
      "availability": "string",
      "conversation": {
        "id": "string",
        "uri": "string"
      },
      "conversationId": 1,
      "creationTime": "string",
      "direction": "string",
      "from": {
        "location": "string",
        "phoneNumber": "string"
      },
      "id": "string",
      "lastModifiedTime": "string",
      "messageStatus": "string",
      "priority": "string",
      "readStatus": "string",
      "segmentCount": 1,
      "subject": "string",
      "to": [
        {
          "location": "string",
          "name": "Ava Chen",
          "phoneNumber": "string"
        }
      ],
      "type": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[].contentType` | string |  |
| `attachments[].id` | number |  |
| `attachments[].type` | string |  |
| `attachments[].uri` | string |  |
| `availability` | string |  |
| `conversation.id` | string |  |
| `conversation.uri` | string |  |
| `conversationId` | number |  |
| `creationTime` | string |  |
| `direction` | string |  |
| `from.location` | string |  |
| `from.phoneNumber` | string |  |
| `id` | string |  |
| `lastModifiedTime` | string |  |
| `messageStatus` | string |  |
| `priority` | string |  |
| `readStatus` | string |  |
| `segmentCount` | number |  |
| `subject` | string |  |
| `to[].location` | string |  |
| `to[].name` | string |  |
| `to[].phoneNumber` | string |  |
| `type` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/:accountId/extension/:extensionId/message-store/:messageId` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

