# 5pm: Get Project By Id

Retrieves a project from 5pm by ID.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/get-project-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/get-project-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/get-project-by-id?${params}`, {
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
| `id` | string | yes | Unique identifier of the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "groupId": 1,
      "id": "string",
      "name": "Ava Chen",
      "ownerId": 1,
      "priority": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Project description. |
| `groupId` | number | Project group ID. |
| `id` | string | Project identifier. |
| `name` | string | Project name. |
| `ownerId` | number | Project owner user ID. |
| `priority` | number | Project priority ID. |
| `status` | number | Project status ID. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/projects/getById` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-by-id.md) for the provider-specific parameters and requirements.

