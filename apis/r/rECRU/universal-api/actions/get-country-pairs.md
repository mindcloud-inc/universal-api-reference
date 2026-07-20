# RECRU: Get Country Pairs



```
GET https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/get-country-pairs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RECRU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/get-country-pairs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/get-country-pairs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RECRU API returns.

## Native endpoint

Through the native RECRU API, this operation is `POST` (base URL `https://mindclo.recru.eu/api/json-rpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-pairs.md) for the provider-specific parameters and requirements.

