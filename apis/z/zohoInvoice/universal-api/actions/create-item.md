# Zoho Invoice: Create Item

Creates an item in Zoho Invoice.

```
POST https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Premium Support",
  "rate": "149.99"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Premium Support",
    "rate": "149.99"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the item. Maximum length of the name [100] Example: `Premium Support`. |
| `rate` | number | yes | Per unit price of an item. Example: `149.99`. |
| `description` | string | no | Description for the item. Maximum characters to be used for describing the item [2000] Example: `Monthly support retainer`. |
| `taxId` | string | no | ID of the tax to be associated to the item. Example: `903000000012345`. |
| `sku` | string | no | SKU or the Stock Keeping Unit value of an item, should be unique throughout the product Example: `SKU-001`. |
| `productType` | list<string> | no | Specify the type of an item. It can be either goods or service One of: `goods`, `service`. |
| `isTaxable` | boolean | no | Boolean to track the taxability of the item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxExemptionId` | string | no | ID of the tax exemption applied. Mandatory, if is_taxable is false. Example: `903000000067890`. |
| `hsnOrSac` | string | no | HSN Code Example: `9983`. |
| `satItemKeyCode` | string | no | Add SAT Item Key Code for your goods/services. Example: `81112100`. |
| `unitkeyCode` | string | no | Add Unit Key Code for your goods/services. Example: `E48`. |
| `itemTaxPreferences[]` | array<object> | no | ID of the tax to be associated to the item. |
| `itemTaxPreferences[].taxId` | string | no | ID of the tax to be associated to the item. Example: `903000000012345`. |
| `itemTaxPreferences[].taxSpecification` | string | no | Set whether the tax type is intra/interstate Example: `inter`. |
| `customFields[]` | array<object> | no | Custom fields for an item. |
| `customFields[].customfieldId` | number | no | Unique identifier of the custom field Example: `460000000128045`. |
| `customFields[].value` | string | no | Value of the Custom Field Example: `Blue`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hasAttachment": true,
      "itemId": "string",
      "itemName": "Ava Chen",
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "productType": "string",
      "rate": 1,
      "sku": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date |  |
| `description` | string |  |
| `hasAttachment` | boolean |  |
| `itemId` | string |  |
| `itemName` | string |  |
| `lastModifiedTime` | date |  |
| `name` | string |  |
| `productType` | string |  |
| `rate` | number |  |
| `sku` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `POST /items` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

