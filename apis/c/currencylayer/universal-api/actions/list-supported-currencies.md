# Currencylayer: List Supported Currencies

Retrieves supported currencies from Currencylayer.

```
GET https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/list-supported-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currencylayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/list-supported-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/list-supported-currencies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Currencylayer API returns.

## Native endpoint

Through the native Currencylayer API, this operation is `GET /list` (base URL `https://api.currencylayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-currencies.md) for the provider-specific parameters and requirements.

