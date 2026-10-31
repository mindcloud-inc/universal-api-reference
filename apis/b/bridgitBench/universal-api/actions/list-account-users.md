# Bridgit Bench: List Account Users



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-users?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-users?${params}`, {
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
| `accountId` | number | yes | The Account ID |
| `group` | string | no | Optional parameter to filter results based on user groups |
| `ids` | number | no | (Optional) Filters the result to contain account users that match the ids passed in. Accepts multiple values as an array. |
| `nameSearch` | string | no | (Optional) Searches for users by partial name match (minimum 3 characters). |
| `search` | string | no | (Optional) Searches for users by partial match on name, email address, permission set name, or grouping name. Grouping names are only matched for active users. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/users` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-users.md) for the provider-specific parameters and requirements.

