# MinIO: Delete Bucket Tagging



```
DELETE https://connect.mindcloud.co/v1/universal/minIO/latest/actions/delete-bucket-tagging
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MinIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/minIO/latest/actions/delete-bucket-tagging?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minIO/latest/actions/delete-bucket-tagging?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MinIO API returns.

## Native endpoint

Through the native MinIO API, this operation is `DELETE /:bucket` (base URL `{{credentials.baseApiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bucket-tagging.md) for the provider-specific parameters and requirements.

