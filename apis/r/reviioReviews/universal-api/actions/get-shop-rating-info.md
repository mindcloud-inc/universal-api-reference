# Revi.io Reviews: Get Shop Rating Info

Retrieves shop rating info from Revi.io Reviews.

```
GET https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-shop-rating-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revi.io Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-shop-rating-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-shop-rating-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Envelope containing the returned shop rating object. |
| `success` | boolean | Whether the shop rating request succeeded. |

## Native endpoint

Through the native Revi.io Reviews API, this operation is `GET /shop_info` (base URL `https://api.revi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shop-rating-info.md) for the provider-specific parameters and requirements.

