# ManyReach: Remove Prospect Tag

Deletes a tag from a prospect in ManyReach.

```
DELETE https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/remove-prospect-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/remove-prospect-tag?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/remove-prospect-tag?${params}`, {
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
| `id` | string | no | Prospect ID. |
| `tagId` | string | no | Tag ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ManyReach API returns.

## Native endpoint

Through the native ManyReach API, this operation is `DELETE https://api.manyreach.com/api/v2/prospects/:id/tags/:tagId` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-prospect-tag.md) for the provider-specific parameters and requirements.

