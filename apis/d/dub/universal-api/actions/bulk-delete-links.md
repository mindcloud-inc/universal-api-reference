# Dub: Bulk Delete Links

Deletes links from Dub in bulk.

```
DELETE https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-delete-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-delete-links?connectionId=$CONNECTION_ID&linkIds%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkIds[]": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-delete-links?${params}`, {
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
| `linkIds[]` | array<string> | yes | Comma-separated list of link IDs to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dub API returns.

## Native endpoint

Through the native Dub API, this operation is `DELETE /links/bulk` (base URL `https://api.dub.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-delete-links.md) for the provider-specific parameters and requirements.

