# CheckFlow: Delete Tag



```
DELETE https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-tag?connectionId=$CONNECTION_ID&tagKey=835bf84f-2068-4c20-9c27-4bfac6efccfc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagKey": "835bf84f-2068-4c20-9c27-4bfac6efccfc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-tag?${params}`, {
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
| `tagKey` | string | yes | The key of the tag to delete. Example: `835bf84f-2068-4c20-9c27-4bfac6efccfc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CheckFlow API returns.

## Native endpoint

Through the native CheckFlow API, this operation is `DELETE /api/tag` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag.md) for the provider-specific parameters and requirements.

