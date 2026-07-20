# actiTIME: List Projects

Retrieves a list of projects from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-projects?${params}`, {
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
| `archived` | boolean | no | Filter archived vs active projects. |
| `customerIds` | string | no | Comma-separated customer ids to retrieve projects from. |
| `ids` | string | no | Comma-separated ids of projects to be returned. |
| `includeReferenced` | string | no | Comma-separated referenced objects to include. |
| `name` | string | no | Exact project name match, case-insensitive. |
| `sort` | string | no | Sorting tokens like +name or -created. |
| `words` | string | no | Return projects containing all given words in the name. |

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
      "archived": true,
      "created": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "customerName": "Ava Chen",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedActions.canDelete` | boolean | Whether the project can be deleted. |
| `allowedActions.canModify` | boolean | Whether the project can be modified. |
| `archived` | boolean | Whether the project is archived. |
| `created` | date | Creation date and time. |
| `customerId` | number | Customer identifier. |
| `customerName` | string | Customer name. |
| `description` | string | Project description. |
| `id` | number | Unique project identifier. |
| `name` | string | Project name. |
| `url` | string | Project URL. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /projects` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

