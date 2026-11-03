# Rithum for Brands: Create a Product



```
POST https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-a-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-a-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileID": 1,
  "sku": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-a-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileID": 1,
    "sku": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileID` | list<number> | yes |  |
| `sku` | string | yes |  |
| `title` | string | yes |  |
| `ASIN` | string | no |  |
| `ShortDescription` | string | no |  |
| `Height` | number | no |  |
| `Length` | number | no |  |
| `Width` | number | no |  |
| `Weight` | number | no |  |
| `StoreTitle` | string | no |  |
| `brand` | string | no |  |
| `manufacturer` | string | no |  |
| `mPN` | string | no |  |
| `condition` | string | no |  |
| `description` | string | no |  |
| `uPC` | string | no |  |
| `ParentSku` | string | no |  |
| `buyItNowPrice` | number | no |  |
| `retailPrice` | number | no |  |
| `isParent` | boolean | no |  |
| `isInRelationship` | boolean | no |  |
| `parentProductID` | number | no |  |
| `Condition` | string | no |  |
| `WarehouseLocation` | string | no |  |
| `RelationshipName` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rithum for Brands API returns.

## Native endpoint

Through the native Rithum for Brands API, this operation is `POST Products` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-product.md) for the provider-specific parameters and requirements.

