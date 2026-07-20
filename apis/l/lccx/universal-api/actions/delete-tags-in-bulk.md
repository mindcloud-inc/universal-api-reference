# lc.cx: Delete Tags in Bulk

Deletes tags in bulk from lc.cx.

```
DELETE https://connect.mindcloud.co/v1/universal/lccx/latest/actions/delete-tags-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lc.cx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/delete-tags-in-bulk?connectionId=$CONNECTION_ID&tagIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lccx/latest/actions/delete-tags-in-bulk?${params}`, {
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
| `tagIds[]` | array<string> | yes | An array of tag IDs to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native lc.cx API returns.

## Native endpoint

Through the native lc.cx API, this operation is `POST /tags/delete/bulk` (base URL `https://api.lc.cx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tags-in-bulk.md) for the provider-specific parameters and requirements.

