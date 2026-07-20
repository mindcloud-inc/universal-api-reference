# NHTSA vPIC: List WMIs for Manufacturer

Retrieves WMIs for a manufacturer from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-wmis-for-manufacturer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-wmis-for-manufacturer?connectionId=$CONNECTION_ID&manufacturer=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "manufacturer": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-wmis-for-manufacturer?${params}`, {
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
| `manufacturer` | string | no | A manufacturer ID or a full or partial manufacturer name. |
| `manufacturer` | string | yes | Manufacturer name fragment or manufacturer ID. |
| `vehicleType` | string | no | Optional vehicle type ID or full or partial vehicle type name to narrow the WMI results. |
| `vehicleType` | string | no | Optional vehicle type name fragment or vehicle type ID to narrow the WMI list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "createdOn": "string",
      "dateAvailableToPublic": "string",
      "id": 1,
      "name": "Ava Chen",
      "updatedOn": "string",
      "vehicleType": "string",
      "wmi": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `createdOn` | string |  |
| `dateAvailableToPublic` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updatedOn` | string |  |
| `vehicleType` | string |  |
| `wmi` | string |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetWMIsForManufacturer/:manufacturer` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-wmis-for-manufacturer.md) for the provider-specific parameters and requirements.

