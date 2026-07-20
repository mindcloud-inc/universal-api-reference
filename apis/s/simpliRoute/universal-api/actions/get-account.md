# SimpliRoute: Get Account

Retrieves the authenticated account from SimpliRoute.

```
GET https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpliRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-account?${params}`, {
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
      "account": {},
      "blocked": true,
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "gps_config": {},
      "has_suscription_id": true,
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
      "modified": "2026-05-07T12:00:00.000Z",
      "modules": [
        {}
      ],
      "name": "Ava Chen",
      "old_id": 1,
      "organization": {},
      "phone": "string",
      "role": {},
      "status": "string",
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `blocked` | boolean |  |
| `created` | date |  |
| `email` | string |  |
| `gps_config` | object |  |
| `has_suscription_id` | boolean |  |
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
| `modified` | date |  |
| `modules` | array<object> |  |
| `name` | string |  |
| `old_id` | number |  |
| `organization` | object |  |
| `phone` | string |  |
| `role` | object |  |
| `status` | string |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native SimpliRoute API, this operation is `GET /v1/accounts/me/` (base URL `https://api.simpliroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

