# Swit: List Users

Retrieves users from Swit with paginated results.

```
GET https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-users?connectionId=$CONNECTION_ID&cnt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cnt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-users?${params}`, {
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
| `cnt` | number | yes | Number of users to return per page. |
| `page` | number | no | Page number to fetch. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bg_color": "string",
      "created": "string",
      "email": "ava@example.com",
      "is_active": true,
      "language": "string",
      "last_activity": "string",
      "mode": "string",
      "msg": "string",
      "photo": "string",
      "role": 1,
      "status": "string",
      "team": [
        [
          {}
        ]
      ],
      "tel": "string",
      "timezone": "string",
      "timezone_auto_flag": 1,
      "user_id": "string",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bg_color` | string |  |
| `created` | string |  |
| `email` | string |  |
| `is_active` | boolean |  |
| `language` | string |  |
| `last_activity` | string |  |
| `mode` | string |  |
| `msg` | string |  |
| `photo` | string |  |
| `role` | number |  |
| `status` | string |  |
| `team[]` | array<object> |  |
| `team[].main_dept_yn` | string |  |
| `team[].team_id` | string |  |
| `team[].team_name` | string |  |
| `tel` | string |  |
| `timezone` | string |  |
| `timezone_auto_flag` | number |  |
| `user_id` | string |  |
| `user_name` | string |  |

## Native endpoint

Through the native Swit API, this operation is `GET organization.user.list` (base URL `https://openapi.swit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

