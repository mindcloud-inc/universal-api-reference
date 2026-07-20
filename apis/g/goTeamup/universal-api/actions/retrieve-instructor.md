# GoTeamup: Retrieve Instructor

Retrieves an instructor from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-instructor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-instructor?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-instructor?${params}`, {
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
| `id` | number | yes | The TeamUp instructor ID. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `object` | string |  |
| `permissions.attendances` | boolean |  |
| `permissions.customerPayments` | boolean |  |
| `permissions.customers` | boolean |  |
| `permissions.developer` | boolean |  |
| `permissions.discountCodes` | boolean |  |
| `permissions.emailNotifications` | boolean |  |
| `permissions.instructorAttendances` | boolean |  |
| `permissions.instructorManageEvents` | boolean |  |
| `permissions.manageEvents` | boolean |  |
| `permissions.pos` | boolean |  |
| `permissions.revenue` | boolean |  |
| `permissions.store` | boolean |  |
| `permissions.superAdmin` | boolean |  |
| `pictureUrl` | object |  |
| `staff` | number |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /instructors/:id` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-instructor.md) for the provider-specific parameters and requirements.

