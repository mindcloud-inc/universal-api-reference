# ServiceTitan: List Vendors

Retrieves vendors from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-vendors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-vendors?${params}`, {
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
| `ids` | string | no |  |
| `active` | string | no |  |
| `createdBefore` | string | no |  |
| `createdOnOrAfter` | string | no |  |
| `externalDataApplicationGuid` | string | no |  |
| `externalDataKey` | string | no |  |
| `externalDataValues` | string | no |  |
| `includeTotal` | boolean | no |  |
| `modifiedBefore` | string | no |  |
| `modifiedOnOrAfter` | string | no |  |
| `sort` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address": {
        "city": {},
        "country": {},
        "state": {},
        "street": "string",
        "unit": "string",
        "zip": {}
      },
      "contactInfo": {
        "email": {},
        "fax": {},
        "firstName": {},
        "lastName": {},
        "phone": "string"
      },
      "createdOn": "string",
      "defaultTaxRate": 1,
      "deliveryOption": "string",
      "externalData": {},
      "id": 1,
      "isMobileCreationRestricted": true,
      "isTruckReplenishment": true,
      "memo": "string",
      "modifiedOn": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address.city` | object |  |
| `address.country` | object |  |
| `address.state` | object |  |
| `address.street` | string |  |
| `address.unit` | string |  |
| `address.zip` | object |  |
| `contactInfo.email` | object |  |
| `contactInfo.fax` | object |  |
| `contactInfo.firstName` | object |  |
| `contactInfo.lastName` | object |  |
| `contactInfo.phone` | string |  |
| `createdOn` | string |  |
| `defaultTaxRate` | number |  |
| `deliveryOption` | string |  |
| `externalData` | object |  |
| `id` | number |  |
| `isMobileCreationRestricted` | boolean |  |
| `isTruckReplenishment` | boolean |  |
| `memo` | string |  |
| `modifiedOn` | string |  |
| `name` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET inventory/v2/tenant/{{credentials.tenant}}/vendors` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-vendors.md) for the provider-specific parameters and requirements.

