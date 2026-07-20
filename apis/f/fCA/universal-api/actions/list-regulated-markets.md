# FCA: List regulated markets



```
GET https://connect.mindcloud.co/v1/universal/fCA/latest/actions/list-regulated-markets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FCA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fCA/latest/actions/list-regulated-markets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fCA/latest/actions/list-regulated-markets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FCA API returns.

## Native endpoint

Through the native FCA API, this operation is `GET /CommonSearch` (base URL `https://register.fca.org.uk/services/V0.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-regulated-markets.md) for the provider-specific parameters and requirements.

