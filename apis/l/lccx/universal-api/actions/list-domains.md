# lc.cx: List Domains

Retrieves branded domains from lc.cx.

```
GET https://connect.mindcloud.co/v1/universal/lccx/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lc.cx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lccx/latest/actions/list-domains?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native lc.cx API returns.

## Native endpoint

Through the native lc.cx API, this operation is `GET /domains` (base URL `https://api.lc.cx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

