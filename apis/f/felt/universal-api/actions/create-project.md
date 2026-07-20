# Felt: Create Project

Creates a new project in Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "visibility": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "visibility": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Project name. |
| `visibility` | string | yes | Project visibility. Felt docs support workspace or private. |
| `maxInheritedPermission` | string | no | Maximum permission workspace members inherit on workspace-visible projects. |

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
| `id` | string | Felt project ID. |
| `maps` | array<object> | Maps currently in the project. |
| `max_inherited_permission` | string | Maximum inherited permission for workspace-visible projects. |
| `name` | string | Project name. |
| `type` | string | Returned resource type. |
| `visibility` | string | Project visibility. |

## Native endpoint

Through the native Felt API, this operation is `POST /projects` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

