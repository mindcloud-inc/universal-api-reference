# MinIO: Put Bucket Versioning



```
PUT https://connect.mindcloud.co/v1/universal/minIO/latest/actions/put-bucket-versioning
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MinIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/minIO/latest/actions/put-bucket-versioning" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minIO/latest/actions/put-bucket-versioning', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MinIO API returns.

## Native endpoint

Through the native MinIO API, this operation is `PUT /:bucket` (base URL `{{credentials.baseApiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-bucket-versioning.md) for the provider-specific parameters and requirements.

