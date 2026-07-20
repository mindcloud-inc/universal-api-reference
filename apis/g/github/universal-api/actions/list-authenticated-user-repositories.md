# GitHub: List Authenticated User Repositories

Lists GitHub repositories for the authenticated user.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-authenticated-user-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-authenticated-user-repositories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-authenticated-user-repositories?${params}`, {
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
| `visibility` | string | no | Repository visibility to return. One of: `0`, `1`, `2`. |
| `affiliation` | string | no | Repository affiliation values to include. One of: `0`, `1`, `2`. Accepts multiple values in one string, delimited by `,`. |
| `type` | string | no | Repository type to return. GitHub ignores this parameter when visibility or affiliation is supplied. One of: `0`, `1`, `2`, `3`, `4`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | string | no | Only show repositories updated after this time (ISO 8601). |
| `before` | string | no | Only show repositories updated before this time (ISO 8601). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `GET /user/repos` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-authenticated-user-repositories.md) for the provider-specific parameters and requirements.

