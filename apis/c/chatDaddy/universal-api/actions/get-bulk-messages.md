# ChatDaddy: Get Bulk Messages

Retrieves bulk message records from ChatDaddy.

```
GET https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/get-bulk-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/get-bulk-messages?connectionId=$CONNECTION_ID&ids%5B%5D=sample-bulk-message-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "sample-bulk-message-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/get-bulk-messages?${params}`, {
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
| `ids[]` | array<string> | yes | Message ids to fetch in bulk. Default: `["sample-bulk-message-id"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "chatId": "string",
      "createdAt": "string",
      "id": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `chatId` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `text` | string |  |

## Native endpoint

Through the native ChatDaddy API, this operation is `GET /messages/bulk` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-messages.md) for the provider-specific parameters and requirements.

