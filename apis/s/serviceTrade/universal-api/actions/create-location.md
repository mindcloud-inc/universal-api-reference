# ServiceTrade: Create Location

Creates a new location in ServiceTrade.

```
POST https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "name": "Ava Chen",
  "addressStreet": "string",
  "addressCity": "string",
  "addressState": "string",
  "addressPostalCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "name": "Ava Chen",
    "addressStreet": "string",
    "addressCity": "string",
    "addressState": "string",
    "addressPostalCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Company to attach the new location to. |
| `name` | string | yes | Name of the new location. |
| `addressStreet` | string | yes | Street address for the new location. |
| `addressCity` | string | yes | City for the new location. |
| `addressState` | string | yes | State or province for the new location. |
| `addressPostalCode` | string | yes | Postal code for the new location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "postalCode": "string",
        "state": "string",
        "street": "string"
      },
      "company": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string",
        "uri": "string"
      },
      "created": 1,
      "email": "ava@example.com",
      "externalIds": {
        "quickbooks": "string"
      },
      "generalManager": "string",
      "geocodeQuality": 1,
      "id": 1,
      "lat": 1,
      "lon": 1,
      "name": "Ava Chen",
      "offices": [
        {
          "address": {
            "city": "string",
            "postalCode": "string",
            "state": "string",
            "street": "string"
          },
          "email": "ava@example.com",
          "id": 1,
          "lat": 1,
          "lon": 1,
          "name": "Ava Chen",
          "phoneNumber": "string",
          "refNumber": "string",
          "status": "string",
          "taxable": true,
          "uri": "string"
        }
      ],
      "phoneNumber": "string",
      "primaryContact": {
        "alternatePhone": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen",
        "mobile": "string",
        "phone": "string",
        "type": "string",
        "types": [
          "string"
        ],
        "uri": "string"
      },
      "refNumber": "string",
      "status": "string",
      "taxable": true,
      "updated": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `address.street` | string |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `company.status` | string |  |
| `company.uri` | string |  |
| `created` | number |  |
| `email` | string |  |
| `externalIds.quickbooks` | string |  |
| `generalManager` | string |  |
| `geocodeQuality` | number |  |
| `id` | number |  |
| `lat` | number |  |
| `lon` | number |  |
| `name` | string |  |
| `offices[].address.city` | string |  |
| `offices[].address.postalCode` | string |  |
| `offices[].address.state` | string |  |
| `offices[].address.street` | string |  |
| `offices[].email` | string |  |
| `offices[].id` | number |  |
| `offices[].lat` | number |  |
| `offices[].lon` | number |  |
| `offices[].name` | string |  |
| `offices[].phoneNumber` | string |  |
| `offices[].refNumber` | string |  |
| `offices[].status` | string |  |
| `offices[].taxable` | boolean |  |
| `offices[].uri` | string |  |
| `phoneNumber` | string |  |
| `primaryContact.alternatePhone` | string |  |
| `primaryContact.email` | string |  |
| `primaryContact.firstName` | string |  |
| `primaryContact.id` | number |  |
| `primaryContact.lastName` | string |  |
| `primaryContact.mobile` | string |  |
| `primaryContact.phone` | string |  |
| `primaryContact.type` | string |  |
| `primaryContact.types[]` | string |  |
| `primaryContact.uri` | string |  |
| `refNumber` | string |  |
| `status` | string |  |
| `taxable` | boolean |  |
| `updated` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native ServiceTrade API, this operation is `POST location` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

