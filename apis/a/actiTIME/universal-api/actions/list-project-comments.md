# actiTIME: List Project Comments

Retrieves comments for a project in actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-project-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-project-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-project-comments?${params}`, {
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
| `id` | number | yes | Project identifier. |
| `includeReferenced` | string | no | Comma-separated referenced objects to include. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native actiTIME API returns.

## Native endpoint

Through the native actiTIME API, this operation is `GET /projects/:id/comments` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-comments.md) for the provider-specific parameters and requirements.

