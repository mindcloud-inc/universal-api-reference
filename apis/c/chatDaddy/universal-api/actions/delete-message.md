# ChatDaddy: Delete Message

Deletes an existing message from ChatDaddy.

```
DELETE https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-message?connectionId=$CONNECTION_ID&accountId=acc_9d2c3b61-174e-42c5-be_0804&chatId=sample-chat-id&id=sample-message-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "acc_9d2c3b61-174e-42c5-be_0804",
  "chatId": "sample-chat-id",
  "id": "sample-message-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-message?${params}`, {
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
| `accountId` | string | yes | Account identifier for the message. Default: `acc_9d2c3b61-174e-42c5-be_0804`. |
| `chatId` | string | yes | Chat identifier for the message. Default: `sample-chat-id`. |
| `id` | string | yes | Message identifier to delete. Default: `sample-message-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the message deletion request completed successfully. |

## Native endpoint

Through the native ChatDaddy API, this operation is `DELETE /messages/{accountId}/{chatId}/{id}` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

