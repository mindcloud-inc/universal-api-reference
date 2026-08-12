# Simpro: Create Site



```
POST https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "0",
  "Name": "MindCloud Test Site"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "0",
    "Name": "MindCloud Test Site"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Simpro company ID. Single-company builds usually use 0. Default: `0`. Example: `0`. |
| `Name` | string | yes | Site name. Example: `MindCloud Test Site`. |
| `Customers[]` | array<number> | no | Customer IDs linked to the site. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "archived": true,
      "billingAddress": {
        "address": "string",
        "city": "string",
        "postalCode": "string",
        "state": "string"
      },
      "billingContact": "string",
      "customers": [
        {
          "companyName": "Ava Chen",
          "familyName": "Ava Chen",
          "givenName": "Ava Chen",
          "id": 1
        }
      ],
      "dateModified": "string",
      "id": 1,
      "name": "Ava Chen",
      "primaryContact": {
        "cellPhone": "string",
        "contact": {},
        "email": "ava@example.com",
        "familyName": "Ava Chen",
        "fax": "string",
        "givenName": "Ava Chen",
        "position": "string",
        "preferredNotificationMethod": "string",
        "title": "string",
        "workPhone": "string"
      },
      "privateNotes": "string",
      "publicNotes": "string",
      "rates": {
        "serviceFee": {}
      },
      "sTCZone": {},
      "vEECZone": {},
      "zone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `archived` | boolean |  |
| `billingAddress.address` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.postalCode` | string |  |
| `billingAddress.state` | string |  |
| `billingContact` | string |  |
| `customers[].companyName` | string |  |
| `customers[].familyName` | string |  |
| `customers[].givenName` | string |  |
| `customers[].id` | number |  |
| `dateModified` | string |  |
| `id` | number |  |
| `name` | string |  |
| `primaryContact.cellPhone` | string |  |
| `primaryContact.contact` | object |  |
| `primaryContact.email` | string |  |
| `primaryContact.familyName` | string |  |
| `primaryContact.fax` | string |  |
| `primaryContact.givenName` | string |  |
| `primaryContact.position` | string |  |
| `primaryContact.preferredNotificationMethod` | string |  |
| `primaryContact.title` | string |  |
| `primaryContact.workPhone` | string |  |
| `privateNotes` | string |  |
| `publicNotes` | string |  |
| `rates.serviceFee` | object |  |
| `sTCZone` | object |  |
| `vEECZone` | object |  |
| `zone` | object |  |

## Native endpoint

Through the native Simpro API, this operation is `POST /companies/:companyId/sites/` (base URL `{{credentials.buildUrl}}/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

