# HRBLADE: List Users



```
GET https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/list-users?${params}`, {
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
      "code": 1,
      "error": true,
      "response": {
        "data": [
          {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "email": "ava@example.com",
            "id": 1,
            "name": "Ava Chen",
            "role": "string",
            "updatedAt": "2026-05-07T12:00:00.000Z"
          }
        ],
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Provider status code. |
| `error` | boolean | Error indicator. |
| `response.data[].createdAt` | date | User creation timestamp. |
| `response.data[].email` | string | User email. |
| `response.data[].id` | number | User identifier. |
| `response.data[].name` | string | User name. |
| `response.data[].role` | string | User role. |
| `response.data[].updatedAt` | date | User update timestamp. |
| `response.message` | string | Optional response message. |

## Native endpoint

Through the native HRBLADE API, this operation is `GET /users` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

