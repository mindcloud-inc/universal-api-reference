# Bump.sh: Set Default Branch

Sets the default branch for a Bump.sh documentation.

```
PUT https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/set-default-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bump.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/set-default-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "doc_id_or_slug": "string",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/set-default-branch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "doc_id_or_slug": "string",
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `doc_id_or_slug` | string | yes | Documentation ID or slug. |
| `slug` | string | yes | Branch slug to promote. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bump.sh API returns.

## Native endpoint

Through the native Bump.sh API, this operation is `PATCH docs/:doc_id_or_slug/branches/:slug/set_default` (base URL `https://bump.sh/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-default-branch.md) for the provider-specific parameters and requirements.

