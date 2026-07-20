# ServiceTrade: Get Location by ID

Retrieves a location from ServiceTrade by ID.

```
GET https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-location-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-location-by-id?connectionId=$CONNECTION_ID&locationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-location-by-id?${params}`, {
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
| `locationId` | number | yes |  |

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

Through the native ServiceTrade API, this operation is `GET location/:locationId` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-by-id.md) for the provider-specific parameters and requirements.

