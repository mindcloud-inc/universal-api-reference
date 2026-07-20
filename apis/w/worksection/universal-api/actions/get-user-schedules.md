# Worksection: Get User Schedules



```
GET https://connect.mindcloud.co/v1/universal/worksection/latest/actions/get-user-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksection `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksection/latest/actions/get-user-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksection/latest/actions/get-user-schedules?${params}`, {
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
      "department": "string",
      "email": "ava@example.com",
      "group": "string",
      "id": "string",
      "name": "Ava Chen",
      "schedule": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `department` | string |  |
| `email` | string |  |
| `group` | string |  |
| `id` | string |  |
| `name` | string |  |
| `schedule` | object |  |

## Native endpoint

Through the native Worksection API, this operation is `GET /` (base URL `https://min7657.worksection.com/api/admin/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-schedules.md) for the provider-specific parameters and requirements.

