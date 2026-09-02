# ClickUp: Search Workspace Docs

Finds Docs in a ClickUp Workspace.

```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/search-workspace-docs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/search-workspace-docs?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/search-workspace-docs?${params}`, {
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
| `archived` | boolean | no | Include archived docs filter |
| `creator` | number | no | Filter by creator user ID |
| `cursor` | string | no | Cursor for pagination |
| `deleted` | boolean | no | Include deleted docs filter |
| `id` | string | no | Filter by document ID |
| `limit` | number | no | Maximum number of docs to return |
| `nextCursor` | string | no | Forward pagination cursor |
| `parentId` | string | no | Filter by parent entity ID |
| `parentType` | string | no | Filter by parent entity type |
| `workspaceId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": [
        {
          "archived": true,
          "archived_by": 1,
          "creator": 1,
          "date_archived": 1,
          "date_created": 1,
          "date_deleted": 1,
          "date_updated": 1,
          "deleted": true,
          "deleted_by": 1,
          "id": "string",
          "name": "Ava Chen",
          "parent": {
            "id": "string",
            "type": 1
          },
          "public": true,
          "type": 1,
          "workspace_id": 1
        }
      ],
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array |  |
| `docs[].archived` | boolean |  |
| `docs[].archived_by` | number |  |
| `docs[].creator` | number |  |
| `docs[].date_archived` | number |  |
| `docs[].date_created` | number |  |
| `docs[].date_deleted` | number |  |
| `docs[].date_updated` | number |  |
| `docs[].deleted` | boolean |  |
| `docs[].deleted_by` | number |  |
| `docs[].id` | string |  |
| `docs[].name` | string |  |
| `docs[].parent` | object |  |
| `docs[].parent.id` | string |  |
| `docs[].parent.type` | number |  |
| `docs[].public` | boolean |  |
| `docs[].type` | number |  |
| `docs[].workspace_id` | number |  |
| `next_cursor` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET https://api.clickup.com/api/v3/workspaces/:workspace_id/docs` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-workspace-docs.md) for the provider-specific parameters and requirements.

