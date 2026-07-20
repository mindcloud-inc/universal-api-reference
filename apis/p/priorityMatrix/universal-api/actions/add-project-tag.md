# Priority Matrix: Add Project Tag

Adds a tag to a Priority Matrix project.

```
POST https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/add-project-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/add-project-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/add-project-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object` | string | yes | Project resource URI to tag. |
| `name` | string | yes | Tag name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Priority Matrix API returns.

## Native endpoint

Through the native Priority Matrix API, this operation is `POST /api/v1/tag/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-tag.md) for the provider-specific parameters and requirements.

