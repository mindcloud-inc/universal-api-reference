# Tableau Cloud: Query Projects

Retrieves a list of projects from Tableau Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "contentPermissions": "string",
      "controllingPermissionsProjectId": "string",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "parentProjectId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentPermissions` | string | Project content permission mode. |
| `controllingPermissionsProjectId` | string | Permissions-controlling project ID. |
| `createdAt` | string | Creation timestamp. |
| `description` | string | Project description. |
| `id` | string | Project ID. |
| `name` | string | Project name. |
| `parentProjectId` | string | Parent project ID. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `GET /sites/site-id/projects` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-projects.md) for the provider-specific parameters and requirements.

