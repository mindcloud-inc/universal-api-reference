# ClustDoc: Search Users



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-users?connectionId=$CONNECTION_ID&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-users?${params}`, {
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
| `search` | string | yes | Search text for users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "lastname": "Chen",
      "phone_number": "string",
      "role": "string",
      "team_id": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `lastname` | string |  |
| `phone_number` | string |  |
| `role` | string |  |
| `team_id` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /users` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-users.md) for the provider-specific parameters and requirements.

