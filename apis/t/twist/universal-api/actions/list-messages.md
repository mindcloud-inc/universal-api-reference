# Twist: List Messages

Retrieves messages from a Twist conversation.

```
GET https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-messages?connectionId=$CONNECTION_ID&conversationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-messages?${params}`, {
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
| `conversationId` | number | yes | The id of the conversation. |
| `limit` | number | no | Limits the number of messages returned. |
| `orderBy` | string | no | Either desc or asc based on obj_index. |

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

Through the native Twist API, this operation is `GET /conversation_messages/get` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

