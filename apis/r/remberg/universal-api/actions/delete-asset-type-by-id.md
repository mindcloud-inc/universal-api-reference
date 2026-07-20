# remberg: Delete Asset Type By Id

Deletes an asset type from remberg by internal ID.

```
DELETE https://connect.mindcloud.co/v1/universal/remberg/latest/actions/delete-asset-type-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a remberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/remberg/latest/actions/delete-asset-type-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remberg/latest/actions/delete-asset-type-by-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native remberg API returns.

## Native endpoint

Through the native remberg API, this operation is `DELETE /v2/assets/types/{id}` (base URL `https://api.remberg.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-asset-type-by-id.md) for the provider-specific parameters and requirements.

