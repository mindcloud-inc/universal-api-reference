# actiTIME: List Workflow Statuses

Retrieves a list of workflow statuses from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-workflow-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-workflow-statuses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-workflow-statuses?${params}`, {
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
| `ids` | string | no | Comma-separated workflow status ids to be returned. |
| `name` | string | no | Exact workflow status name match, case-insensitive. |
| `sort` | string | no | Sorting tokens like +name or -type. |
| `type` | string | no | Workflow status group such as open or completed. |
| `words` | string | no | Return workflow statuses containing all given words in the name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedActions": {
        "canDelete": true,
        "canModify": true
      },
      "id": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedActions.canDelete` | boolean | Whether the workflow status can be deleted. |
| `allowedActions.canModify` | boolean | Whether the workflow status can be modified. |
| `id` | number | Unique workflow status identifier. |
| `name` | string | Workflow status name. |
| `type` | string | Workflow status group. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /workflowStatuses` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflow-statuses.md) for the provider-specific parameters and requirements.

