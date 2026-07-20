# Bump.sh: Create Branch

Creates a new branch in Bump.sh.

```
POST https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bump.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "doc_id_or_slug": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-branch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "doc_id_or_slug": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `doc_id_or_slug` | string | yes | Documentation ID or slug. |
| `name` | string | yes | Branch name to create. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bump.sh API returns.

## Native endpoint

Through the native Bump.sh API, this operation is `POST docs/:doc_id_or_slug/branches` (base URL `https://bump.sh/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-branch.md) for the provider-specific parameters and requirements.

