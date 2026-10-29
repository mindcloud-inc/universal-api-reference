# TikTok Shop: Calculate Refund



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/calculate-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/calculate-refund?connectionId=$CONNECTION_ID&shopCipher=string&orderId=string&requestType=CANCEL&reasonName=Ava%20Chen&skus%5B%5D.skuId=string&skus%5B%5D.quantity=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shopCipher": "string",
  "orderId": "string",
  "requestType": "CANCEL",
  "reasonName": "Ava Chen",
  "skus[].skuId": "string",
  "skus[].quantity": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/calculate-refund?${params}`, {
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
| `shopCipher` | string | yes |  |
| `orderId` | string | yes |  |
| `requestType` | list<string> | yes | One of: `CANCEL`, `REFUND`, `RETURN_AND_REFUND`. |
| `reasonName` | string | yes | Use a reason name returned by Get Aftersale Eligibility for the selected order. |
| `skus[].skuId` | string | yes |  |
| `skus[].quantity` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipmentType` | list<string> | no | One of: `BUYER_ARRANGE`, `PLATFORM`. |
| `handoverMethod` | list<string> | no | One of: `DROP_OFF`, `PICKUP`. |
| `orderLineItemIds[]` | array<string> | no | Choose either these IDs or Order Line List. Omit all item selectors to estimate the entire order. |
| `skus[]` | array<object> | no |  |
| `orderLineList[]` | array<object> | no |  |
| `orderLineList[].orderLineItemId` | string | no |  |
| `orderLineList[].subOrderLineItemId` | string | no | Required for an item within a bundle; optional for other products. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST /return_refund/202602/refunds/calculate` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-refund.md) for the provider-specific parameters and requirements.

