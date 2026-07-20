# Trafft: List Employees

Retrieves employees from Trafft.

```
GET https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trafft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-employees?${params}`, {
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
      "data": {
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "phone_country_code": "string",
        "phone_number": "string",
        "timezone": "string"
      },
      "pagination": {
        "limit": 1,
        "page": 1,
        "pages": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.email` | string |  |
| `data.first_name` | string |  |
| `data.id` | number |  |
| `data.last_name` | string |  |
| `data.phone_country_code` | string |  |
| `data.phone_number` | string |  |
| `data.timezone` | string |  |
| `pagination` | object |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native Trafft API, this operation is `GET /employees` (base URL `https://mindcloud.admin.trafft.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

