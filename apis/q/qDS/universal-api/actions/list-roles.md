# QDS: List Roles



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-roles?${params}`, {
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
      "roles": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": 1,
          "key": "string",
          "name": "Ava Chen",
          "updated_at": "2026-05-07T12:00:00.000Z"
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
| `roles[].created_at` | date |  |
| `roles[].description` | string |  |
| `roles[].id` | number |  |
| `roles[].key` | string |  |
| `roles[].name` | string |  |
| `roles[].updated_at` | date |  |

## Native endpoint

Through the native QDS API, this operation is `GET /roles` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

