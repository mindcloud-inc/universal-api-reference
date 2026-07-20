# inFlow Inventory: Insert or Update Vendor

Inserts or updates a vendor in inFlow Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-vendor', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "contactName": "Ava Chen",
      "currencyId": "string",
      "defaultAddressId": "string",
      "defaultCarrier": "string",
      "defaultPaymentMethod": "string",
      "defaultPaymentTermsId": "string",
      "discount": "string",
      "email": "ava@example.com",
      "fax": "string",
      "isActive": true,
      "isTaxInclusivePricing": true,
      "lastModifiedById": "string",
      "lastModifiedDttm": "2026-05-07T12:00:00.000Z",
      "leadTimeDays": 1,
      "name": "Ava Chen",
      "phone": "string",
      "remarks": "string",
      "taxingSchemeId": "string",
      "timestamp": "string",
      "vendorId": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactName` | string |  |
| `currencyId` | string |  |
| `defaultAddressId` | string |  |
| `defaultCarrier` | string |  |
| `defaultPaymentMethod` | string |  |
| `defaultPaymentTermsId` | string |  |
| `discount` | string |  |
| `email` | string |  |
| `fax` | string |  |
| `isActive` | boolean |  |
| `isTaxInclusivePricing` | boolean |  |
| `lastModifiedById` | string |  |
| `lastModifiedDttm` | date |  |
| `leadTimeDays` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `remarks` | string |  |
| `taxingSchemeId` | string |  |
| `timestamp` | string |  |
| `vendorId` | string |  |
| `website` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `PUT /vendors` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-or-update-vendor.md) for the provider-specific parameters and requirements.

