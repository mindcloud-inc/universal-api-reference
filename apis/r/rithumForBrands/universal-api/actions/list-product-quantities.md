# Rithum for Brands: List Product Quantities

Retrieve Quantities for a specified Product at all Distribution Centers.

```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-product-quantities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-product-quantities?connectionId=$CONNECTION_ID&prodID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prodID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-product-quantities?${params}`, {
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
| `id` | string | no | The Rithum-defined unique ID (not the Sku value) of the product. *Bugged* |
| `prodID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableQuantity": 1,
      "distributionCenterID": 1,
      "productID": 1,
      "profileID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableQuantity` | number |  |
| `distributionCenterID` | number |  |
| `productID` | number |  |
| `profileID` | number |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `GET Products(:prodID)/DCQuantities` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-quantities.md) for the provider-specific parameters and requirements.

