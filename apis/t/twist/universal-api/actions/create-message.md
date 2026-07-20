# Twist: Create Message

Creates a new message in a Twist conversation.

```
POST https://connect.mindcloud.co/v1/universal/twist/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twist/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "conversationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twist/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "conversationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments` | string | no | JSON-encoded list of attachment objects returned by Upload attachment. |
| `content` | string | yes | The content of the new message. |
| `conversationId` | number | yes | The id of the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {
          "attachmentId": "string",
          "fileName": "Ava Chen",
          "fileSize": 1,
          "title": "string",
          "underlyingType": "string",
          "uploadState": "string",
          "url": "https://example.com",
          "urlType": "https://example.com"
        }
      ],
      "content": "string",
      "conversationId": 1,
      "creator": 1,
      "creatorName": "Ava Chen",
      "deleted": true,
      "id": 1,
      "objIndex": 1,
      "postedTs": "string",
      "version": 1,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[].attachmentId` | string |  |
| `attachments[].fileName` | string |  |
| `attachments[].fileSize` | number |  |
| `attachments[].title` | string |  |
| `attachments[].underlyingType` | string |  |
| `attachments[].uploadState` | string |  |
| `attachments[].url` | string |  |
| `attachments[].urlType` | string |  |
| `content` | string |  |
| `conversationId` | number |  |
| `creator` | number |  |
| `creatorName` | string |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `objIndex` | number |  |
| `postedTs` | string |  |
| `version` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Twist API, this operation is `POST /conversation_messages/add` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

