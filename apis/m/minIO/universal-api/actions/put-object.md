# MinIO: Put Object



```
POST https://connect.mindcloud.co/v1/universal/minIO/latest/actions/put-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MinIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minIO/latest/actions/put-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minIO/latest/actions/put-object', {
  method: 'POST',
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

Through the native MinIO API, this operation is `PUT /:bucket/:key` (base URL `{{credentials.baseApiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-object.md) for the provider-specific parameters and requirements.

