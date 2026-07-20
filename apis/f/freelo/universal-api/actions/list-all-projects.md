# Freelo: List All Projects

Retrieves all accessible projects from Freelo.

```
GET https://connect.mindcloud.co/v1/universal/freelo/latest/actions/list-all-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freelo `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freelo/latest/actions/list-all-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freelo/latest/actions/list-all-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Freelo API returns.

## Native endpoint

Through the native Freelo API, this operation is `GET /all-projects` (base URL `https://api.freelo.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-projects.md) for the provider-specific parameters and requirements.

