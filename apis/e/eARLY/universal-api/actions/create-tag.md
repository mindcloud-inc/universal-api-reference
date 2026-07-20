# EARLY: Create Tag

Creates a new tag in EARLY.

```
POST https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "label": "string",
  "scope": "string",
  "folderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "label": "string",
    "scope": "string",
    "folderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | External tag key. |
| `label` | string | yes | Tag label. |
| `scope` | string | yes | Tag scope. |
| `folderId` | string | yes | Folder ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `POST /api/v4/tags` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

