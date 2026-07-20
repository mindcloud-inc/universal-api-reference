# Easy Projects: Get Project Members

Retrieves members of a specific Easy Projects project.

```
GET https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-members?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-members?${params}`, {
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
| `id` | string | yes | Birdview project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "projectId": 1,
      "role": {},
      "roleId": 1,
      "roleName": "Ava Chen",
      "user": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `projectId` | number |  |
| `role` | object |  |
| `roleId` | number |  |
| `roleName` | string |  |
| `user` | object |  |
| `userId` | number |  |

## Native endpoint

Through the native Easy Projects API, this operation is `GET /api/v1/projects/:id/members` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-project-members.md) for the provider-specific parameters and requirements.

