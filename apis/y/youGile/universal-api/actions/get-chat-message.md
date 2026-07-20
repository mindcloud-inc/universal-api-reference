# YouGile: Get chat message

Retrieves a chat message from YouGile.

```
GET https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouGile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-chat-message?connectionId=$CONNECTION_ID&chatId=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-chat-message?${params}`, {
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
| `chatId` | string | yes | The YouGile chat ID. |
| `id` | number | yes | The YouGile message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "editTimestamp": 1,
      "fromUserId": "string",
      "id": 1,
      "label": "string",
      "reactions": {},
      "text": "string",
      "textHtml": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `editTimestamp` | number |  |
| `fromUserId` | string |  |
| `id` | number |  |
| `label` | string |  |
| `reactions` | object |  |
| `text` | string |  |
| `textHtml` | string |  |

## Native endpoint

Through the native YouGile API, this operation is `GET /chats/:chatId/messages/:id` (base URL `{{credentials.companyDomain}}/api-v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-message.md) for the provider-specific parameters and requirements.

