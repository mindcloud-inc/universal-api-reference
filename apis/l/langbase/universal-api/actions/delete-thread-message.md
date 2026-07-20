# Langbase: Delete Thread Message



```
DELETE https://connect.mindcloud.co/v1/universal/langbase/latest/actions/delete-thread-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/delete-thread-message?connectionId=$CONNECTION_ID&threadId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/delete-thread-message?${params}`, {
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
| `threadId` | string | yes | Thread ID that owns the message. |
| `messageId` | string | yes | Message ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sucess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sucess` | boolean |  |

## Native endpoint

Through the native Langbase API, this operation is `DELETE v1/threads/:threadId/messages/:messageId` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-thread-message.md) for the provider-specific parameters and requirements.

