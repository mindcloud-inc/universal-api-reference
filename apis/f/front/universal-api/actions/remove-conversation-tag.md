# Front: Remove Conversation Tag

Removes a tag from a conversation in Front.

```
DELETE https://connect.mindcloud.co/v1/universal/front/latest/actions/remove-conversation-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/front/latest/actions/remove-conversation-tag?connectionId=$CONNECTION_ID&conversationId=cnv_123&tagIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "cnv_123",
  "tagIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/remove-conversation-tag?${params}`, {
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
| `conversationId` | string | yes | The conversation ID. Example: `cnv_123`. |
| `tagIds[]` | array<string> | yes | Tag IDs to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. The saved successful response was an empty string (HTTP 204). |

## Native endpoint

Through the native Front API, this operation is `DELETE /conversations/:conversation_id/tags` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-conversation-tag.md) for the provider-specific parameters and requirements.

