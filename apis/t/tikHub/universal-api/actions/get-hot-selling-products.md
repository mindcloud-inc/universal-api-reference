# TikHub: Get Hot Selling Products

Retrieves hot-selling TikTok Shop products from TikHub.

```
GET https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-hot-selling-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-hot-selling-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-hot-selling-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | string | no | Region code |
| `count` | number | no | Number of products to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |

## Native endpoint

Through the native TikHub API, this operation is `GET /api/v1/tiktok/shop/web/fetch_hot_selling_products_list` (base URL `https://api.tikhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hot-selling-products.md) for the provider-specific parameters and requirements.

