# Priority Matrix: Remove Project Tag

Removes a tag from a Priority Matrix project.

```
DELETE https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/remove-project-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/remove-project-tag?connectionId=$CONNECTION_ID&object=string&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "object": "string",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/remove-project-tag?${params}`, {
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
| `object` | string | yes | Project resource URI to untag. |
| `name` | string | yes | Tag name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Priority Matrix API returns.

## Native endpoint

Through the native Priority Matrix API, this operation is `POST /api/v1/tag/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-tag.md) for the provider-specific parameters and requirements.

