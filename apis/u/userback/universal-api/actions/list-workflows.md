# Userback: List Workflows

Lists the workflows available in Userback.

```
GET https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-workflows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-workflows?${params}`, {
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
      "color": "string",
      "id": 1,
      "name": "Ava Chen",
      "project": {
        "created": "string",
        "createdBy": 1,
        "id": 1,
        "isArchived": true,
        "name": "Ava Chen"
      },
      "sort": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | number |  |
| `name` | string |  |
| `project.created` | string |  |
| `project.createdBy` | number |  |
| `project.id` | number |  |
| `project.isArchived` | boolean |  |
| `project.name` | string |  |
| `sort` | number |  |

## Native endpoint

Through the native Userback API, this operation is `GET /workflow` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

