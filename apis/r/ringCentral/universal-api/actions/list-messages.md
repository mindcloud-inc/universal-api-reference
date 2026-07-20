# RingCentral: List Messages

Retrieves messages from a RingCentral extension.

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string&extensionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string",
  "extensionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-messages?${params}`, {
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
| `messageType` | string | no |  |
| `dateTo` | string | no |  |

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
      "extensionId": "string",
      "from": {
        "location": "string",
        "phoneNumber": "string"
      },
      "id": 1,
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
| `extensionId` | string |  |
| `from.location` | string |  |
| `from.phoneNumber` | string |  |
| `id` | number |  |
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

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/:accountId/extension/:extensionId/message-store` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

