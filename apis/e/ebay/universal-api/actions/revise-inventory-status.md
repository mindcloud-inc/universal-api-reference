# eBay: Revise Inventory Status

Change the price and/or quantity of up to four active, fixed-price listings.

```
PUT https://connect.mindcloud.co/v1/universal/ebay/latest/actions/revise-inventory-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/revise-inventory-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ebay/latest/actions/revise-inventory-status', {
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
| `inventoryStatus[]` | array | no | One InventoryStatus container is required for each item or item variation that is being revised. Whether updating the price and/or quantity of a single-variation listing or a specific variation within a multiple-variation listing, the limit of items or item variations that can be modified with one call is four. |
| `inventoryStatus[].itemID` | string | no | The unique identifier of the listing being revised. - For a single-variation listing, either the ItemID of the listing or the SKU value of the item (if it exists) is required, and which one to use will depend on the value of the InventoryTrackingMethod setting. If the value of InventoryTrackingMethod is ItemID, the ItemID field should be used. If the value of InventoryTrackingMethod is SKU, the SKU field should be used. ItemID is the default value of InventoryTrackingMethod, and its value can only be set/changed to SKU through either an AddFixedPriceItem or RelistFixedPriceItem call. - For a multiple-variation listing, the SKU value of the item variation is required in order to identify a specific item variation. An ItemID field is also required if the InventoryTrackingMethod value is set to ItemID. However, if the InventoryTrackingMethod value is set to SKU, only the SKU value of the item variation is needed to identify a specific item variation. Note that a seller-defined SKU value is required when a seller creates a multiple-variation listing, regardless of whether they decide to track inventory by Item ID or SKU. Note: When using an LMS_REVISE_INVENTORY_STATUS upload feed in Sell Feed API to revise the price and/or quantity for multiple SKUs for a multiple-SKU listing, you must include both the ItemID and SKU values for each variation. See the Upload flow and Inventory upload feed types for more information. Please also note that the same ItemID value can be used multiple times in the same call if you revise several item variations from the same multiple-variation listing. *The ItemID field is always returned in the response, even if an ItemID value was not included in the request.* |
| `inventoryStatus[].quantity` | number | no | This field is used to update the quantity of a fixed-price listing, or to update the quantity of a variation within a multiple-variation listing. To update a variation, both the ItemID and SKU fields are required to identify the listing and the specific variation within that listing, respectively. In each InventoryStatus container, either StartPrice or Quantity (or both) are required. Note: The Quantity field should no longer appear in the response payload. If it does appear, it can be ignored. Sellers can leverage the GetItem call to verify that the requested quantity updates were successful. |
| `inventoryStatus[].sku` | string | no | This value is the seller-defined SKU value of the item being revised. For a single-variation listing, either the ItemID of the listing or the SKU value of the item (if it exists) is required, and which one to use will depend on the value of the InventoryTrackingMethod setting. If the value of InventoryTrackingMethod is ItemID, the ItemID field should be used. If the value of InventoryTrackingMethod is SKU, the SKU field should be used. ItemID is the default value of InventoryTrackingMethod, and its value can only be set/changed to SKU through either an AddFixedPriceItem or RelistFixedPriceItem call. For a multiple-variation listing, the SKU value of the item variation is required in order to identify a specific item variation. An ItemID field is also required if the InventoryTrackingMethod value is set to ItemID. However, if the InventoryTrackingMethod value is set to SKU, only the SKU value of the item variation is needed to identify a specific item variation. Note that a seller-defined SKU value is required when a seller creates a multiple-variation listing, regardless of whether they decide to track inventory by Item ID or SKU. Note: When using an LMS_REVISE_INVENTORY_STATUS upload feed in Sell Feed API to revise the price and/or quantity for multiple SKUs for a multiple-SKU listing, you must include both the ItemID and SKU values for each variation. See the Upload flow and Inventory upload feed types for more information. The SKU field is always returned in the response, and if a SKU value doesn't exist for a single-variation listing, it is returned as an empty tag. |
| `inventoryStatus[].startPrice` | string | no | This field is used to update the price of a fixed-price item, or to update the price of an item variation within a multiple-variation listing. To update the price of an item variation, both the ItemID and SKU fields are required to identify the listing and the specific variation within that listing, respectively. In each InventoryStatus container, either StartPrice or Quantity (or both) are required. Note: The StartPrice field should no longer appear in the response payload. If it does appear, it can be ignored. Sellers can leverage the GetItem call to verify that the requested price updates were successful. See: Insertion Fees eBay.com Listing Fees |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eBay API returns.

## Native endpoint

Through the native eBay API, this operation is `POST` (base URL `https://api.ebay.com/ws/api.dll`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revise-inventory-status.md) for the provider-specific parameters and requirements.

