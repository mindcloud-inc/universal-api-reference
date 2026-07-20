# Cloudsmith: List Repositories for Current User



```
GET https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/list-repositories-for-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudsmith `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/list-repositories-for-current-user?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/list-repositories-for-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloudsmith API returns.

## Native endpoint

Through the native Cloudsmith API, this operation is `GET /repos/` (base URL `https://api.cloudsmith.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-repositories-for-current-user.md) for the provider-specific parameters and requirements.

