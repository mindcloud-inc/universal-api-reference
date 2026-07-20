# NHTSA vPIC: List Makes for Manufacturer and Year

Retrieves makes for a manufacturer and year from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-makes-for-manufacturer-and-year
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-makes-for-manufacturer-and-year?connectionId=$CONNECTION_ID&manufacturer=string&year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "manufacturer": "string",
  "year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-makes-for-manufacturer-and-year?${params}`, {
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
| `year` | number | yes | Model year that must fall within the make year range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "makeId": 1,
      "makeName": "Ava Chen",
      "mfrId": 1,
      "mfrName": "Ava Chen"
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
| `mfrId` | number |  |
| `mfrName` | string |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetMakesForManufacturerAndYear/:manufacturer` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-makes-for-manufacturer-and-year.md) for the provider-specific parameters and requirements.

