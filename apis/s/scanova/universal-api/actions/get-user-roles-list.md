# Scanova: Get User Roles List



```
GET https://connect.mindcloud.co/v1/universal/scanova/latest/actions/get-user-roles-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/get-user-roles-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/get-user-roles-list?${params}`, {
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
      "id": 1,
      "is_custom": true,
      "name": "Ava Chen",
      "permissions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `is_custom` | boolean |  |
| `name` | string |  |
| `permissions` | array<object> |  |

## Native endpoint

Through the native Scanova API, this operation is `GET /multi-users/access-levels/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-roles-list.md) for the provider-specific parameters and requirements.

