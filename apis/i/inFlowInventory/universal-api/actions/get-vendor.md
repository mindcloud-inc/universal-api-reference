# inFlow Inventory: Get Vendor

Retrieves an existing vendor from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-vendor?connectionId=$CONNECTION_ID&vendorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vendorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-vendor?${params}`, {
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
| `vendorId` | string | yes | The inFlow vendor ID. |

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

Through the native inFlow Inventory API, this operation is `GET /vendors/:vendorId` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor.md) for the provider-specific parameters and requirements.

