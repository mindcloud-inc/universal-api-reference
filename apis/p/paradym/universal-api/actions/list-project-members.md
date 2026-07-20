# Paradym: List Project Members

Retrieves project members from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-project-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-project-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-project-members?${params}`, {
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
      "data": [
        {
          "createdAt": "string",
          "id": "string",
          "isOwner": true,
          "project": {
            "name": "Ava Chen"
          },
          "updatedAt": "string",
          "user": {
            "email": "ava@example.com"
          }
        }
      ],
      "meta": {
        "page": {
          "maxSize": "string",
          "size": "string"
        },
        "sort": [
          {
            "id": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdAt` | string |  |
| `data[].id` | string |  |
| `data[].isOwner` | boolean |  |
| `data[].project.name` | string |  |
| `data[].updatedAt` | string |  |
| `data[].user.email` | string |  |
| `meta.page.maxSize` | string |  |
| `meta.page.size` | string |  |
| `meta.sort[].id` | string |  |

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/members` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-members.md) for the provider-specific parameters and requirements.

