# Dashly: Remove Conversation Tag

Deletes a tag from a Dashly conversation.

```
DELETE https://connect.mindcloud.co/v1/universal/dashly/latest/actions/remove-conversation-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/remove-conversation-tag?connectionId=$CONNECTION_ID&id=string&tag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "tag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashly/latest/actions/remove-conversation-tag?${params}`, {
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
| `id` | string | yes |  |
| `tag` | string | yes |  |
| `fromAdmin` | string | no | Default: `default_admin`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dashly API returns.

## Native endpoint

Through the native Dashly API, this operation is `DELETE conversations/:id/tag` (base URL `https://api.dashly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-conversation-tag.md) for the provider-specific parameters and requirements.

