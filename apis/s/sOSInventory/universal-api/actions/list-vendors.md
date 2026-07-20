# SOS Inventory: List Vendors

Retrieves vendors from SOS Inventory.

```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-vendors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-vendors?${params}`, {
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
| `query` | string | no | Filter by matches on the vendor name or notes. |

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

Through the native SOS Inventory API, this operation is `GET /api/v2/vendor` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vendors.md) for the provider-specific parameters and requirements.

