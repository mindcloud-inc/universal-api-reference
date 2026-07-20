# NHTSA vPIC: List Manufacturers

Retrieves manufacturers from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-manufacturers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-manufacturers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-manufacturers?${params}`, {
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
| `manufacturerType` | string | no | Optional manufacturer type name or partial name to narrow the manufacturer list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "mfrCommonName": "Ava Chen",
      "mfrID": 1,
      "mfrName": "Ava Chen",
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
| `country` | string |  |
| `mfrCommonName` | string |  |
| `mfrID` | number |  |
| `mfrName` | string |  |
| `vehicleTypes` | array<object> |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetAllManufacturers` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-manufacturers.md) for the provider-specific parameters and requirements.

