# Lumin: List Workspace Members



```
GET https://connect.mindcloud.co/v1/universal/lumin/latest/actions/list-workspace-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/list-workspace-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lumin/latest/actions/list-workspace-members?${params}`, {
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
| `page` | number | no | Which page of members to return. Default: `1`. |
| `limit` | number | no | How many members to return. One of 10, 25, or 50. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "email": "ava@example.com",
          "id": "string",
          "joinedAt": 1,
          "lastActiveAt": 1,
          "name": "Ava Chen",
          "role": "string"
        }
      ],
      "limit": 1,
      "page": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].email` | string |  |
| `data[].id` | string |  |
| `data[].joinedAt` | number |  |
| `data[].lastActiveAt` | number |  |
| `data[].name` | string |  |
| `data[].role` | string |  |
| `limit` | number |  |
| `page` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Lumin API, this operation is `GET /workspaces/members` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspace-members.md) for the provider-specific parameters and requirements.

