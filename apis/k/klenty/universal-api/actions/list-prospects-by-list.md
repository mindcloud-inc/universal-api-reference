# Klenty: List Prospects By List

Retrieves prospects from a Klenty list.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-list?connectionId=$CONNECTION_ID&limit=25&offset=0&listName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "listName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-list?${params}`, {
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
| `listName` | string | yes | List name to filter prospects by. |
| `start` | number | no | Page number to start from. Default: `1`. |
| `limit` | number | no | Maximum number of prospects to return. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignTo": "string",
      "company": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "list": "string",
      "tags": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignTo` | string |  |
| `company` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `list` | string |  |
| `tags` | string |  |

## Native endpoint

Through the native Klenty API, this operation is `GET /prospects` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-prospects-by-list.md) for the provider-specific parameters and requirements.

