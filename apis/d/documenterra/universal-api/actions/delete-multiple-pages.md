# Documenterra: Delete Multiple Pages

Deletes multiple pages from Documenterra.

```
DELETE https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/delete-multiple-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenterra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/delete-multiple-pages?connectionId=$CONNECTION_ID&id=string&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/delete-multiple-pages?${params}`, {
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
| `id` | string | yes | Documenterra project or publication identifier. |
| `ids[]` | array<string> | yes | Page identifiers to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Documenterra API returns.

## Native endpoint

Through the native Documenterra API, this operation is `DELETE /projects/:id/articles` (base URL `https://mindclouddocumenterra.try.documenterra.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-pages.md) for the provider-specific parameters and requirements.

