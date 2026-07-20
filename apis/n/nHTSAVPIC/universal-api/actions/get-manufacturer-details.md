# NHTSA vPIC: Get Manufacturer Details

Retrieves manufacturer details from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/get-manufacturer-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/get-manufacturer-details?connectionId=$CONNECTION_ID&manufacturer=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "manufacturer": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/get-manufacturer-details?${params}`, {
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
| `manufacturer` | string | yes | Manufacturer name fragment or manufacturer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "address2": "string",
      "city": "string",
      "contactEmail": "ava@example.com",
      "contactFax": "string",
      "contactPhone": "string",
      "country": "string",
      "dBAs": "string",
      "equipmentItems": [
        {}
      ],
      "lastUpdated": "string",
      "manufacturerTypes": [
        {}
      ],
      "mfrCommonName": "Ava Chen",
      "mfrID": 1,
      "mfrName": "Ava Chen",
      "otherManufacturerDetails": "string",
      "postalCode": "string",
      "primaryProduct": "string",
      "principalFirstName": "Ava",
      "principalLastName": "Chen",
      "principalPosition": "string",
      "stateProvince": "string",
      "submittedName": "Ava Chen",
      "submittedOn": "string",
      "submittedPosition": "string",
      "vehicleTypes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `contactEmail` | string |  |
| `contactFax` | string |  |
| `contactPhone` | string |  |
| `country` | string |  |
| `dBAs` | string |  |
| `equipmentItems` | array<object> |  |
| `lastUpdated` | string |  |
| `manufacturerTypes` | array<object> |  |
| `mfrCommonName` | string |  |
| `mfrID` | number |  |
| `mfrName` | string |  |
| `otherManufacturerDetails` | string |  |
| `postalCode` | string |  |
| `primaryProduct` | string |  |
| `principalFirstName` | string |  |
| `principalLastName` | string |  |
| `principalPosition` | string |  |
| `stateProvince` | string |  |
| `submittedName` | string |  |
| `submittedOn` | string |  |
| `submittedPosition` | string |  |
| `vehicleTypes` | array<object> |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetManufacturerDetails/:manufacturer` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-manufacturer-details.md) for the provider-specific parameters and requirements.

