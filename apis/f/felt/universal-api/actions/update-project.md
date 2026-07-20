# Felt: Update Project

Updates an existing project in Felt.

```
PUT https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The Felt project ID. |
| `name` | string | no | The new project name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visibility` | string | no | Project visibility: workspace or private. |
| `maxInheritedPermission` | string | no | Maximum permission inherited by workspace members for workspace-visible projects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "maps": [
        {}
      ],
      "max_inherited_permission": "string",
      "name": "Ava Chen",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `maps` | array<object> |  |
| `max_inherited_permission` | string |  |
| `name` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Felt API, this operation is `POST /projects/:projectId/update` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

