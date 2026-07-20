# Bump.sh: Delete Branch

Deletes an existing branch from Bump.sh.

```
DELETE https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/delete-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bump.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/delete-branch?connectionId=$CONNECTION_ID&doc_id_or_slug=string&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "doc_id_or_slug": "string",
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/delete-branch?${params}`, {
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
| `doc_id_or_slug` | string | yes | Documentation ID or slug. |
| `slug` | string | yes | Branch slug to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bump.sh API returns.

## Native endpoint

Through the native Bump.sh API, this operation is `DELETE docs/:doc_id_or_slug/branches/:slug` (base URL `https://bump.sh/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-branch.md) for the provider-specific parameters and requirements.

