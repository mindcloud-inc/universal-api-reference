# Yanado: List Users From List

Retrieves users from a Yanado list.

```
GET https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-users-from-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yanado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-users-from-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-users-from-list?${params}`, {
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
| `listId` | string | yes | Yanado list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Yanado user email |
| `id` | string | Yanado user ID |
| `name` | string | Yanado user name |

## Native endpoint

Through the native Yanado API, this operation is `GET /public-api/lists/:listId/users` (base URL `https://api.yanado.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users-from-list.md) for the provider-specific parameters and requirements.

