# Logiwa Legacy WMS: Insert Purchase Order

By using this endpoint, the users can create single or multiple purchase orders with lines.

All the products used should be defined in the system before creating any purchase orders.

```
POST https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "depositor": "string",
  "inventorySite": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/insert-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "depositor": "string",
    "inventorySite": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `details[].ItemCode` | string | no |  |
| `details[].itemPackType` | string | no |  |
| `details[].quantity` | number | no |  |
| `details[].LineCode` | string | no |  |
| `details[].totalLinePrice` | number | no | Total purchase price of the order line |
| `details[].detailsNote` | string | no |  |
| `addressText` | string | no |  |
| `city` | string | no |  |
| `clientreferenceCode` | string | no |  |
| `code` | string | no |  |
| `country` | string | no |  |
| `depositor` | string | yes |  |
| `details[]` | array<object> | no |  |
| `email` | string | no |  |
| `geoCode` | string | no |  |
| `inventorySite` | string | yes |  |
| `notes` | string | no |  |
| `partyAddressType` | string | no |  |
| `purchaseOrderStatus` | string | no |  |
| `purchaseOrderType` | string | no |  |
| `state` | string | no |  |
| `supplier` | string | no |  |
| `supplierAddress` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/PurchaseOrderBulkInsert` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-purchase-order.md) for the provider-specific parameters and requirements.

