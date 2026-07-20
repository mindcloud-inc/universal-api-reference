# LimoExpress: List Users

Retrieves users from the LimoExpress organization.

```
GET https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-users?${params}`, {
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
| `searchString` | string | no | Search across user fields. |
| `page` | number | no | Page number, default is 1. |
| `perPage` | number | no | Items per page, default is 20. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "client": {},
      "email": "ava@example.com",
      "id": "string",
      "language": "string",
      "last_active_at": "string",
      "passengers_details_visible": 1,
      "profile": {},
      "role": {},
      "timezone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Active flag. |
| `client` | object | Client object when applicable. |
| `email` | string | User email. |
| `id` | string | User identifier. |
| `language` | string | Preferred language. |
| `last_active_at` | string | Last active timestamp. |
| `passengers_details_visible` | number | Passenger details visibility flag. |
| `profile` | object | Profile object. |
| `role` | object | Role object. |
| `timezone` | string | User timezone. |
| `username` | string | Username. |

## Native endpoint

Through the native LimoExpress API, this operation is `GET /api/integration/users` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

