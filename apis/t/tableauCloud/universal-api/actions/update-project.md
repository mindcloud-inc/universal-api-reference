# Tableau Cloud: Update Project

Updates an existing project in Tableau Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Tableau Cloud API, this operation is `PUT /sites/site-id/projects/project-id` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

