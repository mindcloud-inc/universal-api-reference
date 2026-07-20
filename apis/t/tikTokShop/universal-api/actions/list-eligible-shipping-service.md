# TikTok Shop: List Eligible Shipping Service

Use this API ( for US ) to query the list of available shipping services when specifying packages' size or weight. The shipping fee and delivery time is an estimate only and is based on the package dimensions and weight you provided. Options listed may differ if you change the package attributes at the time of shipping.

```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/list-eligible-shipping-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/list-eligible-shipping-service?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/list-eligible-shipping-service?${params}`, {
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
| `dimension.length` | string | no |  |
| `orderId` | string | no |  |
| `weight.value` | string | no |  |
| `dimension.height` | string | no |  |
| `shopCipher` | list | no |  |
| `weight.unit` | list | no | The unit of measurement is used to measure the weight. - GRAM - POUND |
| `dimension.width` | string | no |  |
| `order_line_item_ids` | string | no |  |
| `dimension.unit` | list | no | The unit of measurement is used to measure the length. - CM - INCH |
| `dimension` | object | no |  |
| `weight` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST /fulfillment/202309/orders/:orderId/shipping_services/query` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-eligible-shipping-service.md) for the provider-specific parameters and requirements.

