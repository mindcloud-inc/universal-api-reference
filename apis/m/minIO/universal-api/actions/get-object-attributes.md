# MinIO: Get Object Attributes



```
GET https://connect.mindcloud.co/v1/universal/minIO/latest/actions/get-object-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MinIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minIO/latest/actions/get-object-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minIO/latest/actions/get-object-attributes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MinIO API returns.

## Native endpoint

Through the native MinIO API, this operation is `GET /:bucket/:key` (base URL `{{credentials.baseApiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-object-attributes.md) for the provider-specific parameters and requirements.

