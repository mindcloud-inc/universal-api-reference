# NHTSA vPIC: List Makes for Manufacturer

Retrieves makes for a manufacturer from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-makes-for-manufacturer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-makes-for-manufacturer?connectionId=$CONNECTION_ID&manufacturer=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "manufacturer": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-makes-for-manufacturer?${params}`, {
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
      "makeID": 1,
      "makeName": "Ava Chen",
      "mfrName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `makeID` | number |  |
| `makeName` | string |  |
| `mfrName` | string |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetMakeForManufacturer/:manufacturer` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-makes-for-manufacturer.md) for the provider-specific parameters and requirements.

