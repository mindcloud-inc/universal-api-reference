# eBay: Get SKU Inventory Location

Allows sellers to retrieve the locations mapped to a specific SKU within a listing.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-sku-inventory-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-sku-inventory-location?connectionId=$CONNECTION_ID&listingID=string&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listingID": "string",
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-sku-inventory-location?${params}`, {
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
| `listingID` | string | yes | The unique-id of the listing that the SKU belongs to for which all mapped locations will be retrieved. |
| `sku` | string | yes | The seller-defined SKU value of the item/variation for which location mappings will be retrieved. This SKU value must be defined in the listing specified in the 'Listing ID' parameter above. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eBay API returns.

## Native endpoint

Through the native eBay API, this operation is `GET sell/inventory/v1/listing/:listingID/sku/:sku/locations` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sku-inventory-location.md) for the provider-specific parameters and requirements.

