# GoTeamup: List Instructors

Finds instructors in GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-instructors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-instructors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-instructors?${params}`, {
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
      "count": 1,
      "next": {},
      "previous": {},
      "results": [
        {
          "description": "string",
          "id": 1,
          "name": "Ava Chen",
          "object": "string",
          "permissions": {
            "attendances": true,
            "customerPayments": true,
            "customers": true,
            "developer": true,
            "discountCodes": true,
            "emailNotifications": true,
            "instructorAttendances": true,
            "instructorManageEvents": true,
            "manageEvents": true,
            "pos": true,
            "revenue": true,
            "store": true,
            "superAdmin": true
          },
          "pictureUrl": {},
          "staff": 1
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
| `count` | number |  |
| `next` | object |  |
| `previous` | object |  |
| `results[].description` | string |  |
| `results[].id` | number |  |
| `results[].name` | string |  |
| `results[].object` | string |  |
| `results[].permissions.attendances` | boolean |  |
| `results[].permissions.customerPayments` | boolean |  |
| `results[].permissions.customers` | boolean |  |
| `results[].permissions.developer` | boolean |  |
| `results[].permissions.discountCodes` | boolean |  |
| `results[].permissions.emailNotifications` | boolean |  |
| `results[].permissions.instructorAttendances` | boolean |  |
| `results[].permissions.instructorManageEvents` | boolean |  |
| `results[].permissions.manageEvents` | boolean |  |
| `results[].permissions.pos` | boolean |  |
| `results[].permissions.revenue` | boolean |  |
| `results[].permissions.store` | boolean |  |
| `results[].permissions.superAdmin` | boolean |  |
| `results[].pictureUrl` | object |  |
| `results[].staff` | number |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /instructors` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-instructors.md) for the provider-specific parameters and requirements.

