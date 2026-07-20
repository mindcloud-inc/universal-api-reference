# Cryptlex: List Users

Retrieves users from Cryptlex.

```
GET https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/list-users?${params}`, {
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
| `page` | number | no | Page number. |
| `limit` | number | no | Number of records per page (1-100). |
| `sort` | string | no | Sort expression such as -createdAt. |
| `search` | string | no | Search string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowCustomerPortalAccess": true,
      "company": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "lastLoginAt": "2026-05-07T12:00:00.000Z",
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "role": "string",
      "twoFactorEnabled": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowCustomerPortalAccess` | boolean |  |
| `company` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `lastLoginAt` | date |  |
| `lastSeenAt` | date |  |
| `name` | string |  |
| `role` | string |  |
| `twoFactorEnabled` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Cryptlex API, this operation is `GET /v3/users` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

