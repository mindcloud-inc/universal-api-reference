# CINCEL: List Users



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-users?${params}`, {
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
| `idLike` | string | no | Filter users by partial ID match. |
| `nameLike` | string | no | Filter users by partial name match. |
| `emailLike` | string | no | Filter users by partial email match. |
| `roleLike` | string | no | Filter users by the documented role values. |
| `rfcLike` | string | no | Filter users whose RFC contains this value. |
| `curpLike` | string | no | Filter users whose CURP contains this value. |
| `jobLike` | string | no | Filter users whose job contains this value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CINCEL API returns.

## Native endpoint

Through the native CINCEL API, this operation is `GET /users` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

