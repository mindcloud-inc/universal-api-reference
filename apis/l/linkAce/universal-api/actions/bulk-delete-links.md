# LinkAce: Bulk Delete Links



```
DELETE https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/bulk-delete-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkAce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/bulk-delete-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/bulk-delete-links?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LinkAce API returns.

## Native endpoint

Through the native LinkAce API, this operation is `DELETE /bulk/delete` (base URL `https://demo.linkace.org/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-delete-links.md) for the provider-specific parameters and requirements.

