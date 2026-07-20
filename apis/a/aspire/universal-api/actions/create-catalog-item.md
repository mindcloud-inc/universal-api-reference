# Aspire: Create Catalog Item

Creates a new catalog item in your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-catalog-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-catalog-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "catalogItemCategoryId": 1,
  "itemType": "string",
  "availableToBid": true,
  "active": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-catalog-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "catalogItemCategoryId": 1,
    "itemType": "string",
    "availableToBid": true,
    "active": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `catalogItemCategoryId` | number | yes |  |
| `itemType` | string | yes |  |
| `itemName` | string | no |  |
| `itemAlternateName` | string | no |  |
| `itemDescription` | string | no |  |
| `itemCode` | string | no |  |
| `itemCost` | number | no |  |
| `purchaseUnitTypeId` | number | no |  |
| `allocationUnitTypeId` | number | no |  |
| `unitTypeAllocationConversion` | number | no |  |
| `epaNumber` | string | no |  |
| `epaName` | string | no |  |
| `inventory` | boolean | no |  |
| `availableToBid` | boolean | yes |  |
| `active` | boolean | yes |  |
| `takeoffItemId` | number | no |  |
| `purchaseUnitCost` | number | no |  |
| `forceUnitPricing` | boolean | no |  |
| `allocateFromMobile` | boolean | no |  |
| `catalogId` | number | no |  |
| `materialBarcode1` | string | no |  |
| `materialBarcode2` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `POST CatalogItems` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-catalog-item.md) for the provider-specific parameters and requirements.

