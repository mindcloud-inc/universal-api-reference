# inFlow Inventory: Get Customer

Retrieves an existing customer from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-customer?${params}`, {
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
| `customerId` | string | yes | The inFlow customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactName": "Ava Chen",
      "customerId": "string",
      "defaultBillingAddressId": "string",
      "defaultLocationId": "string",
      "defaultPaymentMethod": "string",
      "defaultPaymentTermsId": "string",
      "defaultSalesRep": "string",
      "defaultSalesRepTeamMemberId": "string",
      "defaultShippingAddressId": "string",
      "discount": "string",
      "email": "ava@example.com",
      "fax": "string",
      "isActive": true,
      "lastModifiedById": "string",
      "lastModifiedDttm": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phone": "string",
      "pricingSchemeId": "string",
      "remarks": "string",
      "taxExemptNumber": "string",
      "taxingSchemeId": "string",
      "timestamp": "string",
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
| `customerId` | string |  |
| `defaultBillingAddressId` | string |  |
| `defaultLocationId` | string |  |
| `defaultPaymentMethod` | string |  |
| `defaultPaymentTermsId` | string |  |
| `defaultSalesRep` | string |  |
| `defaultSalesRepTeamMemberId` | string |  |
| `defaultShippingAddressId` | string |  |
| `discount` | string |  |
| `email` | string |  |
| `fax` | string |  |
| `isActive` | boolean |  |
| `lastModifiedById` | string |  |
| `lastModifiedDttm` | date |  |
| `name` | string |  |
| `phone` | string |  |
| `pricingSchemeId` | string |  |
| `remarks` | string |  |
| `taxExemptNumber` | string |  |
| `taxingSchemeId` | string |  |
| `timestamp` | string |  |
| `website` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `GET /customers/:customerId` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

