# Porter: List Project Invites

Retrieves invites from a Porter project.

```
GET https://connect.mindcloud.co/v1/universal/porter/latest/actions/list-project-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porter/latest/actions/list-project-invites?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porter/latest/actions/list-project-invites?${params}`, {
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
| `projectId` | string | yes | The Porter project ID whose invites you want to list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Porter API returns.

## Native endpoint

Through the native Porter API, this operation is `GET /api/v2/projects/:projectId/invites` (base URL `https://dashboard.porter.run`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-invites.md) for the provider-specific parameters and requirements.

