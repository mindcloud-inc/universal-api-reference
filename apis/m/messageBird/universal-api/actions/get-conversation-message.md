# MessageBird: Get Conversation Message



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation-message?connectionId=$CONNECTION_ID&workspaceId=string&conversationId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "conversationId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-conversation-message?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | string | yes | The Bird conversation ID that owns the message. |
| `messageId` | string | yes | The Bird message ID you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {},
      "conversationId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "draft": true,
      "draftMeta": {},
      "id": "string",
      "inbox": {},
      "interactions": [
        {}
      ],
      "meta": {},
      "reason": "string",
      "receiverTypes": [
        "string"
      ],
      "recipients": [
        {}
      ],
      "reference": "string",
      "replyToMessageId": "string",
      "sender": {},
      "source": "string",
      "status": "string",
      "template": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | object |  |
| `conversationId` | string | Conversation ID. |
| `createdAt` | date | Creation timestamp formatted as RFC3339. |
| `draft` | boolean | Whether this message is a draft. |
| `draftMeta` | object | Metadata for draft messages. |
| `id` | string | Message ID. |
| `inbox` | object | A reference to an inbox. |
| `interactions` | array<object> | A list of interactions associated with the message. |
| `meta` | object | Message metadata fields that might be populated depending on the channel being used. |
| `reason` | string | Failure reason. Will be populated if the status is `sending_failed` or `delivery_failed`. |
| `receiverTypes` | array<string> | ReceiverTypes list of types of receivers for the message. It can be `to`, `cc` and `bcc` at the moment. Currently only use for inbound email platforms messages. |
| `recipients` | array<object> | Recipient list of this message. |
| `reference` | string | A customizable ID assigned to messages you send. This can be used to correlate messages with data from your own integrating services. Must be globally unique within a workspace. |
| `replyToMessageId` | string |  |
| `sender` | object | A participant who can send and receive messages in the conversation |
| `source` | string | Whether the message was created by Bird's Conversations API or an external party. |
| `status` | string | Message status. The lifecycle order is `accepted`, `processing`, `sent`, and `delivered`. |
| `template` | object |  |
| `updatedAt` | date | Update timestamp formatted as RFC3339. |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/conversations/:conversationId/messages/:messageId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-message.md) for the provider-specific parameters and requirements.

