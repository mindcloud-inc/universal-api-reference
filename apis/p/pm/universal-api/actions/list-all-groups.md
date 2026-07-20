# 5pm: List All Groups

Retrieves all project groups from 5pm.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-all-groups?${params}`, {
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
          "id": 1,
          "name": "Ava Chen"
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
| `count` | number | Number of groups in this page. |
| `items[].id` | number | Group identifier. |
| `items[].name` | string | Group name. |
| `total` | number | Total number of groups available. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/projectsgroups/getAll` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-groups.md) for the provider-specific parameters and requirements.

