# Basecamp: Get Message

Retrieves a message from Basecamp.

```
GET https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-message?connectionId=$CONNECTION_ID&accountId=195539477&messageId=1069479406" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "195539477",
  "messageId": "1069479406"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-message?${params}`, {
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
| `messageId` | number | yes | Example: `1069479406`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `GET /:accountId/messages/:messageId.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

