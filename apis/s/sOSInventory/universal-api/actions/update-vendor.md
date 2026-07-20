# SOS Inventory: Update Vendor

Updates an existing vendor in SOS Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "syncTokenValue": "string",
  "vendorBodyId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-vendor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "syncTokenValue": "string",
    "vendorBodyId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The SOS vendor ID to update. |
| `syncTokenValue` | string | yes | The current sync token for this vendor. |
| `vendorBodyId` | number | yes | The SOS vendor ID inside the request body, which must match the path ID. |
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

Through the native SOS Inventory API, this operation is `PUT /api/v2/vendor/:id` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor.md) for the provider-specific parameters and requirements.

