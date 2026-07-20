# KiteSuite: Search Workspace Data

Finds workspace data in KiteSuite by search query.

```
GET https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/search-workspace-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/search-workspace-data?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/search-workspace-data?${params}`, {
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
| `query` | string | yes | Search query string. |
| `selectedType` | string | no | Filter type: task, project, or epic. |
| `projects[]` | array<string> | no | Project IDs to filter by. Pass an array of project IDs. Accepts multiple values as an array. |
| `assignees[]` | array<string> | no | Assignee IDs to filter by. Pass an array of user IDs. Accepts multiple values as an array. |
| `reporters[]` | array<string> | no | Reporter IDs to filter by. Pass an array of user IDs. Accepts multiple values as an array. |
| `status` | string | no | Status filter: done or open. |
| `priorities[]` | array<string> | no | Priorities to filter by. Pass an array such as high or low. Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KiteSuite API returns.

## Native endpoint

Through the native KiteSuite API, this operation is `GET /api/v1/workspace/search/:query` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-workspace-data.md) for the provider-specific parameters and requirements.

