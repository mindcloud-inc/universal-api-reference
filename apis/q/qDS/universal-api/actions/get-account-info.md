# QDS: Get Account Info



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-account-info?${params}`, {
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
      "cycle_start_date": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "num_surveys": 1,
      "num_users": 1,
      "user": {
        "account_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "name": "Ava Chen",
        "role_id": 1,
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cycle_start_date` | date |  |
| `email` | string |  |
| `name` | string |  |
| `num_surveys` | number |  |
| `num_users` | number |  |
| `user.account_id` | number |  |
| `user.created_at` | date |  |
| `user.email` | string |  |
| `user.first_name` | string |  |
| `user.id` | number |  |
| `user.last_name` | string |  |
| `user.name` | string |  |
| `user.role_id` | number |  |
| `user.updated_at` | date |  |

## Native endpoint

Through the native QDS API, this operation is `GET /account/info` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

