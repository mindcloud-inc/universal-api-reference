# Samsara: List Users



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-users?${params}`, {
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
      "authType": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "orgDirectory": "string",
      "roles": [
        {
          "role": {
            "id": "string",
            "name": "Ava Chen"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authType` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `orgDirectory` | string |  |
| `roles[].role.id` | string |  |
| `roles[].role.name` | string |  |

## Native endpoint

Through the native Samsara API, this operation is `GET users` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

