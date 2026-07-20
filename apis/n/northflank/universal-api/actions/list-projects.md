# Northflank: List projects

Retrieves projects for the authenticated Northflank account.

```
GET https://connect.mindcloud.co/v1/universal/northflank/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Northflank `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/northflank/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/northflank/latest/actions/list-projects?${params}`, {
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
      "data": {
        "projects": [
          {
            "description": "string",
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "pagination": {
        "count": 1,
        "cursor": "string",
        "hasNextPage": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.projects` | array<object> | List of projects returned by the Northflank API. |
| `data.projects[].description` | string | Project description. |
| `data.projects[].id` | string | Project identifier. |
| `data.projects[].name` | string | Project name. |
| `pagination.count` | number | Number of returned results. |
| `pagination.cursor` | string | Cursor for the next page. |
| `pagination.hasNextPage` | boolean | Whether another page is available. |

## Native endpoint

Through the native Northflank API, this operation is `GET /projects` (base URL `https://api.northflank.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

