# Zoho Invoice: Update Item

Updates an item in Zoho Invoice.

```
PUT https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "903000000045027",
  "name": "Premium Support",
  "rate": "149.99"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "903000000045027",
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
| `itemId` | string | yes | Example: `903000000045027`. |
| `name` | string | yes | Example: `Premium Support`. |
| `rate` | number | yes | Example: `149.99`. |
| `description` | string | no | Example: `Monthly support retainer`. |
| `taxId` | string | no | Example: `903000000012345`. |
| `sku` | string | no | Example: `SKU-001`. |
| `productType` | list<string> | no | One of: `goods`, `service`. |
| `isTaxable` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxExemptionId` | string | no | Example: `903000000067890`. |
| `hsnOrSac` | string | no | Example: `9983`. |
| `satItemKeyCode` | string | no | Example: `81112100`. |
| `unitkeyCode` | string | no | Example: `E48`. |
| `itemTaxPreferences[]` | array<object> | no |  |
| `itemTaxPreferences[].taxId` | string | no | Example: `903000000012345`. |
| `itemTaxPreferences[].taxSpecification` | string | no | Example: `inter`. |
| `customFields[]` | array<object> | no |  |
| `customFields[].customfieldId` | number | no | Example: `460000000128045`. |
| `customFields[].value` | string | no | Example: `Blue`. |

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

Through the native Zoho Invoice API, this operation is `PUT /items/:item_id` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

