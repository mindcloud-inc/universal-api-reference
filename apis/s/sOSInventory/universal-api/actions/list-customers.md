# SOS Inventory: List Customers

Retrieves customers from SOS Inventory.

```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-customers?${params}`, {
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
| `archived` | string | no | Use yes to return archived records only or no to return active records only. |
| `email` | string | no | Filter by the customer's email. |
| `name` | string | no | Filter by matches on the name or fullname fields. |
| `query` | string | no | Filter by matches on name, fullname, or notes. |

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

Through the native SOS Inventory API, this operation is `GET /api/v2/customer` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

