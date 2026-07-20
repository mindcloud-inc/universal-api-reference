# Cody: List Conversations



```
GET https://connect.mindcloud.co/v1/universal/cody/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cody/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cody/latest/actions/list-conversations?${params}`, {
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
| `botId` | list<string> | no | Id of the bot to filter the list of conversations to only those that are using the selected bot. |
| `keyword` | string | no | Keyword to filter the list of conversations to only those that at least partially match the conversation name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includes` | list<string> | no | Lists document ids the conversation is focused on. One of: `document_ids`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | Selected bot identifier. |
| `createdAt` | date | Conversation creation timestamp. |
| `id` | string | Conversation identifier. |
| `name` | string | Conversation name. |

## Native endpoint

Through the native Cody API, this operation is `GET /conversations` (base URL `https://getcody.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

