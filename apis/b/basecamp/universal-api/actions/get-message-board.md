# Basecamp: Get Message Board

Retrieves a message board from Basecamp.

```
GET https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-message-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-message-board?connectionId=$CONNECTION_ID&accountId=195539477&boardId=1069479392" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "195539477",
  "boardId": "1069479392"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-message-board?${params}`, {
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
| `accountId` | string | yes | Example: `195539477`. |
| `boardId` | number | yes | Example: `1069479392`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `GET /:accountId/message_boards/:boardId.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-board.md) for the provider-specific parameters and requirements.

