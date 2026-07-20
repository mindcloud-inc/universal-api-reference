# JustCall: List All Users

Retrieves users from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-users?${params}`, {
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
| `available` | boolean | no | Filter users by availability. |
| `email` | string | no | Filter users by email address. |
| `groupId` | number | no | Filter users by group ID. |
| `order` | string | no | Sort direction for the returned users. |
| `role` | string | no | Filter users by role. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "currentPage": 1,
      "data": [
        {}
      ],
      "nextPageLink": "https://example.com",
      "perPage": 1,
      "prevPageLink": "https://example.com",
      "status": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `nextPageLink` | string |  |
| `perPage` | number |  |
| `prevPageLink` | string |  |
| `status` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/users` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-users.md) for the provider-specific parameters and requirements.

