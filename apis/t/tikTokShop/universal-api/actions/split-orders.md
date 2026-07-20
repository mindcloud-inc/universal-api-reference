# TikTok Shop: Split Orders

Use this API to confirm an order split. Note that ​​supported split levels vary by region​​:
- Some regions support ​​item-level splits​​ (splitting individual units of the same SKU).
- Others only support ​​all-units splits​​ (splitting different SKUs into separate packages).

Here are two examples of supported splits:
- ​​Case 1: all-units split​​, applicable for orders in BR, SEA, MX (local sellers)
Split a buyer order of SKU A of quantity 2 and SKU B of quantity 1 into two separate packages:
  - ​​Package 1​​: all units of SKU A
​​  - Package 2​​: all units of SKU B

- ​​Case 2: item-level split​​, applicable for orders in EU, JP, MX (global sellers), UK, US
Split the same order contents into three individual packages:
  - ​​Package 1​​: 1 unit of SKU A
​  - ​Package 2​​: 1 unit of SKU A
​​  - Package 3​​: 1 unit of SKU B

```
POST https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/split-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/split-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/split-orders', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `splittableGroups` | object | no | Input list of splittable groups. |
| `splittableGroups.id` | string | no | A unique identifier designated by the developer. This identifier will represent a group of items that will be split into a new package. Once split is confirmed, the platform will be assigned a new package ID for this group of items. For example, if you input 123 as request, the response will return 123 as your unique identification. The seller uses this field to label each group of items that have been split, and the platform will assign new package IDs to them. |
| `orderId` | string | no |  |
| `splittableGroups.orderLineitemids[]` | array | no | The order line item IDs that need to be split into this group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST fulfillment/202309/orders/:order_id/split` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-orders.md) for the provider-specific parameters and requirements.

