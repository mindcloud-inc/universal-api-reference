# SOS Inventory: Create Vendor

Creates a vendor in SOS Inventory.

```
POST https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/create-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/create-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/create-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name by which you look up this vendor. |
| `email` | string | no | Vendor email address. |
| `phone` | string | no | Vendor phone number. |
| `companyName` | string | no | Company name for this vendor. |
| `notes` | string | no | Internal notes about this vendor. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumber": "string",
      "address": {
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
      "altPhone": "string",
      "archived": true,
      "companyName": "Ava Chen",
      "contact": {
        "firstName": {},
        "lastName": {},
        "middleName": {},
        "suffix": {},
        "title": {}
      },
      "currency": {},
      "customFields": {},
      "email": "ava@example.com",
      "fax": "string",
      "id": 1,
      "keys": {},
      "lastSync": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "showOnForms": true,
      "starred": 1,
      "summaryOnly": true,
      "syncMessage": {},
      "syncToken": 1,
      "taxCode": {},
      "terms": {},
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
| `accountNumber` | string |  |
| `address.city` | object |  |
| `address.country` | object |  |
| `address.line1` | object |  |
| `address.line2` | object |  |
| `address.line3` | object |  |
| `address.line4` | object |  |
| `address.line5` | object |  |
| `address.postalCode` | object |  |
| `address.stateProvince` | object |  |
| `altPhone` | string |  |
| `archived` | boolean |  |
| `companyName` | string |  |
| `contact.firstName` | object |  |
| `contact.lastName` | object |  |
| `contact.middleName` | object |  |
| `contact.suffix` | object |  |
| `contact.title` | object |  |
| `currency` | object |  |
| `customFields` | object |  |
| `email` | string |  |
| `fax` | string |  |
| `id` | number |  |
| `keys` | object |  |
| `lastSync` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `showOnForms` | boolean |  |
| `starred` | number |  |
| `summaryOnly` | boolean |  |
| `syncMessage` | object |  |
| `syncToken` | number |  |
| `taxCode` | object |  |
| `terms` | object |  |
| `values` | object |  |
| `website` | string |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `POST /api/v2/vendor` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor.md) for the provider-specific parameters and requirements.

