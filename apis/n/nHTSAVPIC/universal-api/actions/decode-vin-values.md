# NHTSA vPIC: Decode VIN Values

Retrieves flat decoded VIN values from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/decode-vin-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/decode-vin-values?connectionId=$CONNECTION_ID&vin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vin": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/decode-vin-values?${params}`, {
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
| `modelYear` | string | no | Optional model year to improve decoding accuracy for current or pre-1980 VINs. |
| `vin` | string | no | The VIN to decode. Partial VINs are also supported. |
| `vin` | string | yes | Vehicle Identification Number to decode in flat format. Partial VINs are supported with a * placeholder. |
| `modelYear` | number | no | Optional model year used to improve VIN decoding accuracy, especially for partial VINs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyClass": "string",
      "doors": "string",
      "driveType": "string",
      "errorCode": "string",
      "errorText": "string",
      "make": "string",
      "makeID": "string",
      "manufacturer": "string",
      "manufacturerId": "string",
      "model": "string",
      "modelID": "string",
      "modelYear": "string",
      "plantCity": "string",
      "plantCountry": "string",
      "trim": "string",
      "vehicleType": "string",
      "vin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyClass` | string |  |
| `doors` | string |  |
| `driveType` | string |  |
| `errorCode` | string |  |
| `errorText` | string |  |
| `make` | string |  |
| `makeID` | string |  |
| `manufacturer` | string |  |
| `manufacturerId` | string |  |
| `model` | string |  |
| `modelID` | string |  |
| `modelYear` | string |  |
| `plantCity` | string |  |
| `plantCountry` | string |  |
| `trim` | string |  |
| `vehicleType` | string |  |
| `vin` | string |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/DecodeVinValues/:vin` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/decode-vin-values.md) for the provider-specific parameters and requirements.

