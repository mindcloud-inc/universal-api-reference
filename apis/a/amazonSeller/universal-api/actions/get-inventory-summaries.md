# Amazon Seller: Get FBA Inventory Summaries (AFN only)

Retrieves AFN inventory summaries from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-inventory-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-inventory-summaries?connectionId=$CONNECTION_ID&marketplaceIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "marketplaceIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-inventory-summaries?${params}`, {
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
| `marketplaceIds` | list<string> | yes | The marketplace ID of the marketplace for which to return inventory summaries. (max: 1x marketplace) |
| `startDateTime` | string | no | A start date and time - If specified, all inventory summaries that have changed since then are returned. You must specify a date and time that is no earlier than 18 months prior to the date and time when you call the API. Note: Changes in `inboundWorkingQuantity`, `inboundShippedQuantity` and `inboundReceivingQuantity` are not detected. |
| `sellerSkus` | string | no | A list of seller SKUs for which to return inventory summaries. You may specify up to 50 SKUs. Accepts multiple values in one string. |
| `details` | boolean | no | Toggle on to return inventory summaries with additional summarized inventory details and quantities. Otherwise, returns inventory summaries only (default value). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `granularityType` | string | no | The granularity type for the inventory aggregation level. Allowed: `Marketplace` Default: `Marketplace`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asin": "string",
      "condition": "string",
      "fnSku": "string",
      "inventoryDetails": {
        "fulfillableQuantity": 1,
        "futureSupplyQuantity": {
          "futureSupplyBuyableQuantity": 1,
          "reservedFutureSupplyQuantity": 1
        },
        "inboundReceivingQuantity": 1,
        "inboundShippedQuantity": 1,
        "inboundWorkingQuantity": 1,
        "researchingQuantity": {
          "researchingQuantityBreakdown": [
            {
              "name": "Ava Chen",
              "quantity": 1
            }
          ],
          "totalResearchingQuantity": 1
        },
        "reservedQuantity": {
          "fcProcessingQuantity": 1,
          "pendingCustomerOrderQuantity": 1,
          "pendingTransshipmentQuantity": 1,
          "totalReservedQuantity": 1
        },
        "unfulfillableQuantity": {
          "carrierDamagedQuantity": 1,
          "customerDamagedQuantity": 1,
          "defectiveQuantity": 1,
          "distributorDamagedQuantity": 1,
          "expiredQuantity": 1,
          "totalUnfulfillableQuantity": 1,
          "warehouseDamagedQuantity": 1
        }
      },
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "productName": "Ava Chen",
      "sellerSku": "string",
      "totalQuantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asin` | string |  |
| `condition` | string |  |
| `fnSku` | string |  |
| `inventoryDetails.fulfillableQuantity` | number |  |
| `inventoryDetails.futureSupplyQuantity.futureSupplyBuyableQuantity` | number |  |
| `inventoryDetails.futureSupplyQuantity.reservedFutureSupplyQuantity` | number |  |
| `inventoryDetails.inboundReceivingQuantity` | number |  |
| `inventoryDetails.inboundShippedQuantity` | number |  |
| `inventoryDetails.inboundWorkingQuantity` | number |  |
| `inventoryDetails.researchingQuantity.researchingQuantityBreakdown[].name` | string |  |
| `inventoryDetails.researchingQuantity.researchingQuantityBreakdown[].quantity` | number |  |
| `inventoryDetails.researchingQuantity.totalResearchingQuantity` | number |  |
| `inventoryDetails.reservedQuantity.fcProcessingQuantity` | number |  |
| `inventoryDetails.reservedQuantity.pendingCustomerOrderQuantity` | number |  |
| `inventoryDetails.reservedQuantity.pendingTransshipmentQuantity` | number |  |
| `inventoryDetails.reservedQuantity.totalReservedQuantity` | number |  |
| `inventoryDetails.unfulfillableQuantity.carrierDamagedQuantity` | number |  |
| `inventoryDetails.unfulfillableQuantity.customerDamagedQuantity` | number |  |
| `inventoryDetails.unfulfillableQuantity.defectiveQuantity` | number |  |
| `inventoryDetails.unfulfillableQuantity.distributorDamagedQuantity` | number |  |
| `inventoryDetails.unfulfillableQuantity.expiredQuantity` | number |  |
| `inventoryDetails.unfulfillableQuantity.totalUnfulfillableQuantity` | number |  |
| `inventoryDetails.unfulfillableQuantity.warehouseDamagedQuantity` | number |  |
| `lastUpdatedTime` | date |  |
| `productName` | string |  |
| `sellerSku` | string |  |
| `totalQuantity` | number |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET fba/inventory/v1/summaries` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-summaries.md) for the provider-specific parameters and requirements.

