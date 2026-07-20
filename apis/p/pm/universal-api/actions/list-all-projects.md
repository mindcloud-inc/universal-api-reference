# 5pm: List All Projects

Retrieves all projects from 5pm.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-projects?${params}`, {
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
      "count": 1,
      "items": [
        {
          "groupId": 1,
          "id": "string",
          "name": "Ava Chen",
          "ownerId": 1,
          "priority": 1,
          "status": 1
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of projects in this page. |
| `items[].groupId` | number | Project group ID. |
| `items[].id` | string | Project identifier. |
| `items[].name` | string | Project name. |
| `items[].ownerId` | number | Project owner user ID. |
| `items[].priority` | number | Project priority ID. |
| `items[].status` | number | Project status ID. |
| `total` | number | Total number of projects available. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/projects/getAll` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-projects.md) for the provider-specific parameters and requirements.

