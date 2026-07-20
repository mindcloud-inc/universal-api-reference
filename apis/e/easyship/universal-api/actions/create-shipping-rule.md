# Easyship: Create Shipping Rule

Creates a new shipping rule in Easyship.

```
POST https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-shipping-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-shipping-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "conditions[]": [
    {}
  ],
  "conditions[].type": "string",
  "actions[]": [
    {}
  ],
  "actions[].type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-shipping-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string",
    "conditions[]": [{}],
    "conditions[].type": "string",
    "actions[]": [{}],
    "actions[].type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Shipping rule name. |
| `description` | string | yes | Shipping rule description. |
| `recalculateShipments` | boolean | no | Recalculate all shipments affected by this shipping rule. |
| `priority` | number | no | Smaller values represent higher priority. |
| `conditions[]` | array<object> | yes | Array of shipping rule conditions. |
| `conditions[].type` | string | yes | Condition discriminator type. |
| `conditions[].options` | object | no | Condition options object. |
| `conditions[].options.countryIds[]` | array<number> | no | Country IDs for match_country conditions. |
| `conditions[].options.categoryIds[]` | array<string> | no | Category IDs for match_category conditions. |
| `conditions[].options.states[]` | array<string> | no | State codes for match_state conditions. |
| `conditions[].options.operator` | string | no | Operator used by zipcode, SKU, buyer courier, item count, price, or weight conditions. |
| `conditions[].options.zipcodes[]` | array<string> | no | Zipcodes for match_zipcode conditions. |
| `conditions[].options.shipmentItemsSku` | string | no | Shipment item SKU for match_sku conditions. |
| `conditions[].options.platformNames[]` | array<string> | no | Platform names for match_platform_name conditions. |
| `conditions[].options.storeIds[]` | array<string> | no | Store IDs for match_store conditions. |
| `conditions[].options.buyerSelectedCourierName` | string | no | Buyer-selected courier name for match_buyer_selected_courier_name conditions. |
| `conditions[].options.shipmentItemsCount` | number | no | Shipment item count for match_items_count conditions. |
| `conditions[].options.value` | number | no | Numeric value for price-based conditions. |
| `conditions[].options.currency` | string | no | Currency for selling-price conditions. |
| `conditions[].options.totalActualWeight` | number | no | Total actual weight for match_weight conditions. |
| `conditions[].options.orderTagList[]` | array<string> | no | Order tags for include_order_tag_name conditions. |
| `actions[]` | array<object> | yes | Array of shipping rule actions. |
| `actions[].type` | string | yes | Action discriminator type. |
| `actions[].options` | object | no | Action options object. |
| `actions[].options.neverCourierServiceIds[]` | array<string> | no | Courier service IDs to exclude. |
| `actions[].options.preferredCourierServiceIds[]` | array<string> | no | Courier service IDs to prefer. |
| `actions[].options.incoterms` | string | no | Incoterms to force. |
| `actions[].options.sortBy` | string | no | Sorting mode for courier selection. |
| `actions[].options.insured` | boolean | no | Whether to force insurance. |
| `actions[].options.forceTrackingRating[]` | array<number> | no | Tracking ratings to force. |
| `actions[].options.neverPackageIds[]` | array<string> | no | Package IDs to reject. |
| `actions[].options.setAsResidential` | boolean | no | Whether to force residential surcharge behavior. |
| `actions[].options.originAddressId` | string | no | Origin address ID to force. |
| `actions[].options.forceAutomatedReturnRequested` | boolean | no | Whether to force automated returns. |
| `actions[].options.operator` | string | no | Operator for forced delivery time actions. |
| `actions[].options.value` | number | no | Value for forced delivery time actions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessible": true,
      "actions": [
        [
          {}
        ]
      ],
      "active": true,
      "checkoutRestrictive": true,
      "conditions": [
        [
          {}
        ]
      ],
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "priority": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessible` | boolean |  |
| `actions[]` | array<object> |  |
| `actions[].id` | string |  |
| `actions[].type` | string |  |
| `active` | boolean |  |
| `checkoutRestrictive` | boolean |  |
| `conditions[]` | array<object> |  |
| `conditions[].id` | string |  |
| `conditions[].type` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `priority` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `POST /shipping_rules` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipping-rule.md) for the provider-specific parameters and requirements.

