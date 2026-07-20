# GanttPRO: List Users

Retrieves users from your GanttPRO account.

```
GET https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-users?${params}`, {
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
      "dateFormat": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "locale": "string",
      "photo": "string",
      "registrationTime": "2026-05-07T12:00:00.000Z",
      "roleId": 1,
      "settings": {},
      "teamId": 1,
      "timeFormat": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateFormat` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `locale` | string |  |
| `photo` | string |  |
| `registrationTime` | date |  |
| `roleId` | number |  |
| `settings` | object |  |
| `teamId` | number |  |
| `timeFormat` | string |  |
| `username` | string |  |

## Native endpoint

Through the native GanttPRO API, this operation is `GET /users` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

