# SOS Inventory: Update Customer

Updates an existing customer in SOS Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "syncTokenValue": "string",
  "customerBodyId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "syncTokenValue": "string",
    "customerBodyId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The SOS customer ID to update. |
| `syncTokenValue` | string | yes | The current sync token for this customer. |
| `customerBodyId` | number | yes | The SOS customer ID inside the request body, which must match the path ID. |
| `name` | string | yes | The name by which you look up this customer. |
| `email` | string | no | Customer email address. |
| `phone` | string | no | Customer phone number. |
| `companyName` | string | no | Company name for this customer. |
| `notes` | string | no | Internal notes about the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altPhone": "string",
      "archived": true,
      "billing": {
        "city": {},
        "country": {},
        "line1": {},
        "line2": {},
        "line3": {},
        "line4": {},
        "line5": {},
        "postalCode": {},
        "stateProvince": {}
      },
      "billWithParent": true,
      "businessLicense": "string",
      "companyName": "Ava Chen",
      "contact": {
        "firstName": {},
        "lastName": {},
        "middleName": {},
        "suffix": {},
        "title": {}
      },
      "contractorNumber": "string",
      "creditHold": true,
      "currency": {},
      "customerType": {},
      "customFields": {},
      "email": "ava@example.com",
      "expMonth": {},
      "expYear": {},
      "fax": "string",
      "foundUsVia": "string",
      "fullname": "Ava Chen",
      "hasCardOnFile": true,
      "hasChildren": true,
      "id": 1,
      "isInQuickBooks": true,
      "keys": {},
      "lastFour": {},
      "lastSync": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "notes": "string",
      "parent": {},
      "paymentMethod": {},
      "phone": "string",
      "portalPassword": "string",
      "priceTier": {},
      "resaleNumber": "string",
      "salesRep": {},
      "shipping": {
        "city": {},
        "country": {},
        "line1": {},
        "line2": {},
        "line3": {},
        "line4": {},
        "line5": {},
        "postalCode": {},
        "stateProvince": {}
      },
      "starred": 1,
      "sublevel": 1,
      "summaryOnly": true,
      "syncMessage": {},
      "syncToken": 1,
      "tax": {
        "taxable": true,
        "taxCode": {},
        "taxExemptReasonId": {}
      },
      "terms": {},
      "tokenType": {},
      "values": {},
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altPhone` | string |  |
| `archived` | boolean |  |
| `billing.city` | object |  |
| `billing.country` | object |  |
| `billing.line1` | object |  |
| `billing.line2` | object |  |
| `billing.line3` | object |  |
| `billing.line4` | object |  |
| `billing.line5` | object |  |
| `billing.postalCode` | object |  |
| `billing.stateProvince` | object |  |
| `billWithParent` | boolean |  |
| `businessLicense` | string |  |
| `companyName` | string |  |
| `contact.firstName` | object |  |
| `contact.lastName` | object |  |
| `contact.middleName` | object |  |
| `contact.suffix` | object |  |
| `contact.title` | object |  |
| `contractorNumber` | string |  |
| `creditHold` | boolean |  |
| `currency` | object |  |
| `customerType` | object |  |
| `customFields` | object |  |
| `email` | string |  |
| `expMonth` | object |  |
| `expYear` | object |  |
| `fax` | string |  |
| `foundUsVia` | string |  |
| `fullname` | string |  |
| `hasCardOnFile` | boolean |  |
| `hasChildren` | boolean |  |
| `id` | number |  |
| `isInQuickBooks` | boolean |  |
| `keys` | object |  |
| `lastFour` | object |  |
| `lastSync` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `parent` | object |  |
| `paymentMethod` | object |  |
| `phone` | string |  |
| `portalPassword` | string |  |
| `priceTier` | object |  |
| `resaleNumber` | string |  |
| `salesRep` | object |  |
| `shipping.city` | object |  |
| `shipping.country` | object |  |
| `shipping.line1` | object |  |
| `shipping.line2` | object |  |
| `shipping.line3` | object |  |
| `shipping.line4` | object |  |
| `shipping.line5` | object |  |
| `shipping.postalCode` | object |  |
| `shipping.stateProvince` | object |  |
| `starred` | number |  |
| `sublevel` | number |  |
| `summaryOnly` | boolean |  |
| `syncMessage` | object |  |
| `syncToken` | number |  |
| `tax.taxable` | boolean |  |
| `tax.taxCode` | object |  |
| `tax.taxExemptReasonId` | object |  |
| `terms` | object |  |
| `tokenType` | object |  |
| `values` | object |  |
| `website` | string |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `PUT /api/v2/customer/:id` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

