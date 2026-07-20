# SimpliRoute: Get User

Retrieves a driver from SimpliRoute by ID.

```
GET https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpliRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-user?${params}`, {
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
| `userId` | number | yes | The SimpliRoute driver ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app_version": "string",
      "blocked": true,
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "is_admin": true,
      "is_codriver": true,
      "is_coordinator": true,
      "is_driver": true,
      "is_monitor": true,
      "is_owner": true,
      "is_router": true,
      "is_router_jr": true,
      "is_seller": true,
      "is_seller_viewer": true,
      "is_staff": true,
      "last_login": "2026-05-07T12:00:00.000Z",
      "last_mobile_activity": "2026-05-07T12:00:00.000Z",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "old_id": 1,
      "phone": "string",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_version` | string |  |
| `blocked` | boolean |  |
| `created` | date |  |
| `email` | string |  |
| `id` | number |  |
| `is_admin` | boolean |  |
| `is_codriver` | boolean |  |
| `is_coordinator` | boolean |  |
| `is_driver` | boolean |  |
| `is_monitor` | boolean |  |
| `is_owner` | boolean |  |
| `is_router` | boolean |  |
| `is_router_jr` | boolean |  |
| `is_seller` | boolean |  |
| `is_seller_viewer` | boolean |  |
| `is_staff` | boolean |  |
| `last_login` | date |  |
| `last_mobile_activity` | date |  |
| `modified` | date |  |
| `name` | string |  |
| `old_id` | number |  |
| `phone` | string |  |
| `status` | string |  |
| `username` | string |  |

## Native endpoint

Through the native SimpliRoute API, this operation is `GET /v1/accounts/drivers/:user_id/` (base URL `https://api.simpliroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

