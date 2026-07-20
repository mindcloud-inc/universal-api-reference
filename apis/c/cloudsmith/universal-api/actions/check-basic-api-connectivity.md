# Cloudsmith: Check Basic API Connectivity



```
GET https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/check-basic-api-connectivity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudsmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/check-basic-api-connectivity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/check-basic-api-connectivity?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloudsmith API returns.

## Native endpoint

Through the native Cloudsmith API, this operation is `GET /status/check/basic/` (base URL `https://api.cloudsmith.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-basic-api-connectivity.md) for the provider-specific parameters and requirements.

