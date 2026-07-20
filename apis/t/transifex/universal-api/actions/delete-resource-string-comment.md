# Transifex: Delete Resource String Comment



```
DELETE https://connect.mindcloud.co/v1/universal/transifex/latest/actions/delete-resource-string-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/delete-resource-string-comment?connectionId=$CONNECTION_ID&commentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transifex/latest/actions/delete-resource-string-comment?${params}`, {
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
| `commentId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Transifex API returns.

## Native endpoint

Through the native Transifex API, this operation is `DELETE /resource_string_comments/:comment_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-resource-string-comment.md) for the provider-specific parameters and requirements.

