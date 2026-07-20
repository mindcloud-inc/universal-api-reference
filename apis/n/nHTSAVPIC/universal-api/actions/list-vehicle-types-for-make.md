# NHTSA vPIC: List Vehicle Types for Make

Retrieves vehicle types for a make from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-vehicle-types-for-make
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-vehicle-types-for-make?connectionId=$CONNECTION_ID&make=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "make": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-vehicle-types-for-make?${params}`, {
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
| `make` | string | yes | Make name fragment, such as mercedes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "makeId": 1,
      "makeName": "Ava Chen",
      "vehicleTypeId": 1,
      "vehicleTypeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `makeId` | number |  |
| `makeName` | string |  |
| `vehicleTypeId` | number |  |
| `vehicleTypeName` | string |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetVehicleTypesForMake/:make` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicle-types-for-make.md) for the provider-specific parameters and requirements.

