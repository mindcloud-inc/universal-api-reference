# Walmart: Bulk Update Price ( New )

Update the price section in bulk for multiple items. This is useful for implementing pricing strategies across your catalog, such as seasonal discounts, competitive pricing adjustments, or clearance sales.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-update-price-new
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-update-price-new" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-update-price-new', {
  method: 'PUT',
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
| `MPItem[].sku` | string | no | The SKU of the item for which the price is being updated. |
| `MPItem[].price` | number | no | The selling price of the item on Walmart.com. |
| `MPItem[]` | array<object> | no | Add (+) or map items here from a previous step. |
| `MPItem[].msrp` | number | no | The manufacturer's suggested retail price (MSRP) for the item. |
| `MPItem[].businessPrice` | number | no | The business price for the item. Unlike the `price` field, which is visible to everyone, the `businessPrice` is only visible to verified business organizations and non-profits. In the Walmart ecosystem, setting a `businessPrice` that is lower than your standard retail price can help you: - Win the Business Buy Box - Encourage Bulk Purchasing from retailers. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `MPItemFeedHeader` | object | no |  |
| `MPItemFeedHeader.businessUnit` | list<list> | no | The business unit for which the feed is submitted. For example, use 'Walmart_US' for U.S. Marketplace. Default: `WALMART_US`. |
| `MPItemFeedHeader.version` | list<string> | no | The version of the feed schema being used. Please use `5.0.20250328-17_43_36-api` for the PRICE section updates and use `2.0.20240126-12_25_52-api` for PROMO&DISCOUNT section updates. Default: `2.0.20240126-12_25_52-api`. |
| `MPItemFeedHeader.locale` | string | no | The locale code for the content in the feed. For example, `en` for English. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feedId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST v3/feeds` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-price-new.md) for the provider-specific parameters and requirements.

