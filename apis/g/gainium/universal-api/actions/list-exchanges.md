# Gainium: List Exchanges



```
GET https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-exchanges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gainium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-exchanges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-exchanges?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gainium API returns.

## Native endpoint

Through the native Gainium API, this operation is `GET /api/v2/user/exchanges` (base URL `https://api.gainium.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-exchanges.md) for the provider-specific parameters and requirements.

