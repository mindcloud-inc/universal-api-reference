# Deepset: Query Files

Queries files in a Deepset workspace with SQL.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/query-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/query-files?connectionId=$CONNECTION_ID&sql=string&workspaceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sql": "string",
  "workspaceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/query-files?${params}`, {
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
| `sql` | string | yes | SQL query for files. |
| `workspaceName` | string | yes | deepset workspace name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Deepset API returns.

## Native endpoint

Through the native Deepset API, this operation is `POST /api/v1/workspaces/:workspace_name/files/_sql` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-files.md) for the provider-specific parameters and requirements.

