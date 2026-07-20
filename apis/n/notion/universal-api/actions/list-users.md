# Notion: List Users

Retrieves users from the connected Notion workspace.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-users?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSize` | number | no | Number of users to return (max 100). Default: `100`. Example: `100`. |
| `startCursor` | string | no | Pagination cursor returned by previous response. Example: `d7f7f7f7-7f7f-7f7f-7f7f-d7f7f7f7f7f7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": {},
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "person": {
        "email": "ava@example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | object |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `person.email` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Notion API, this operation is `GET /users` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

