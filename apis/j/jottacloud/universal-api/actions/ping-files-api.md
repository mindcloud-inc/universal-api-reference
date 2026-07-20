# Jottacloud: Ping Files API



```
GET https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/ping-files-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jottacloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/ping-files-api?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/ping-files-api?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jottacloud API returns.

## Native endpoint

Through the native Jottacloud API, this operation is `POST /files/v2/ping` (base URL `https://api.jotta.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-files-api.md) for the provider-specific parameters and requirements.

