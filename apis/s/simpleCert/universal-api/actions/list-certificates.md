# SimpleCert: List Certificates



```
GET https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/list-certificates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleCert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/list-certificates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/list-certificates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SimpleCert API returns.

## Native endpoint

Through the native SimpleCert API, this operation is `GET /certificates/list` (base URL `https://app.simplecert.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-certificates.md) for the provider-specific parameters and requirements.

