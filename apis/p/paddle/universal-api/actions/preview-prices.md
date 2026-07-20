# Paddle: Preview Prices

Retrieves a pricing preview from Paddle.

```
GET https://connect.mindcloud.co/v1/universal/paddle/latest/actions/preview-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/preview-prices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paddle/latest/actions/preview-prices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paddle API returns.

## Native endpoint

Through the native Paddle API, this operation is `POST pricing-preview` (base URL `https://api.paddle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-prices.md) for the provider-specific parameters and requirements.

