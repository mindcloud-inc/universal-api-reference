# ContentStudio: List Posts

Retrieves social media posts for a ContentStudio workspace.

```
GET https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-posts?connectionId=$CONNECTION_ID&workspace_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-posts?${params}`, {
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
| `approval_assigned_to[]` | array<string> | no | Filter posts assigned to one or more approver user IDs. |
| `approval_requested_by[]` | array<string> | no | Filter posts requested for approval by one or more user IDs. |
| `date_from` | date | no | Filter posts from this date (YYYY-MM-DD). |
| `date_to` | date | no | Filter posts through this date (YYYY-MM-DD). |
| `page` | number | no | Page number for pagination. |
| `per_page` | number | no | Number of items per page. |
| `status[]` | array<string> | no | Filter posts by one or more status values. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": {},
      "approval": {},
      "campaign": {},
      "content": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "externalActions": [
        {}
      ],
      "externalComments": [
        {}
      ],
      "id": "string",
      "labels": [
        {}
      ],
      "scheduling": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | object |  |
| `approval` | object |  |
| `campaign` | object |  |
| `content` | object |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `externalActions` | array<object> |  |
| `externalComments` | array<object> |  |
| `id` | string |  |
| `labels` | array<object> |  |
| `scheduling` | object |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native ContentStudio API, this operation is `GET /workspaces/:workspace_id/posts` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

