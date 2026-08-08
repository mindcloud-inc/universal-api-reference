# Google Maps: Validate Address

Validates an Address

```
POST https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/validate-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Maps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/validate-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/validate-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | object | no |  |
| `address.regionCode` | string | no | Optional, but helpful for a complete validation. i.e. `CA` for Canada. |
| `address.addressLines` | string | no | Required. Unstructured address lines describing the lower levels of an address. Because values in addressLines do not have type information and may sometimes contain multiple values in a single field (e.g. "Austin, TX"), it is important that the line order is clear. The order of address lines should be "envelope order" for the country/region of the address. The minimum permitted structural representation of an address consists of all information placed in the addressLines. If a regionCode is not provided, the region is inferred from the address lines. Creating an address only containing addressLines, and then geocoding is the recommended way to handle completely unstructured addresses (as opposed to guessing which parts of the address should be localities or administrative areas). Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseId": "string",
      "result": {
        "verdict": {
          "inputGranularity": "string",
          "validationGranularity": "string",
          "geocodeGranularity": "string",
          "addressComplete": true,
          "hasInferredComponents": true,
          "possibleNextAction": "string"
        },
        "address": {
          "formattedAddress": "string",
          "postalAddress": {
            "regionCode": "string",
            "languageCode": "string",
            "postalCode": "string",
            "administrativeArea": "string",
            "locality": "string",
            "addressLines": [
              "string"
            ]
          },
          "addressComponents": [
            {
              "componentName": {
                "text": "Ava Chen"
              },
              "componentType": "string",
              "confirmationLevel": "string"
            }
          ]
        },
        "geocode": {
          "location": {
            "latitude": 1,
            "longitude": 1
          },
          "plusCode": {
            "globalCode": "string"
          },
          "bounds": {
            "low": {
              "latitude": 1,
              "longitude": 1
            },
            "high": {
              "latitude": 1,
              "longitude": 1
            }
          },
          "placeId": "string",
          "placeTypes": [
            "string"
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseId` | string |  |
| `result.verdict.inputGranularity` | string |  |
| `result.verdict.validationGranularity` | string |  |
| `result.verdict.geocodeGranularity` | string |  |
| `result.verdict.addressComplete` | boolean |  |
| `result.verdict.hasInferredComponents` | boolean |  |
| `result.verdict.possibleNextAction` | string |  |
| `result.address.formattedAddress` | string |  |
| `result.address.postalAddress.regionCode` | string |  |
| `result.address.postalAddress.languageCode` | string |  |
| `result.address.postalAddress.postalCode` | string |  |
| `result.address.postalAddress.administrativeArea` | string |  |
| `result.address.postalAddress.locality` | string |  |
| `result.address.postalAddress.addressLines[]` | string |  |
| `result.address.addressComponents[].componentName.text` | string |  |
| `result.address.addressComponents[].componentType` | string |  |
| `result.address.addressComponents[].confirmationLevel` | string |  |
| `result.geocode.location.latitude` | number |  |
| `result.geocode.location.longitude` | number |  |
| `result.geocode.plusCode.globalCode` | string |  |
| `result.geocode.bounds.low.latitude` | number |  |
| `result.geocode.bounds.low.longitude` | number |  |
| `result.geocode.bounds.high.latitude` | number |  |
| `result.geocode.bounds.high.longitude` | number |  |
| `result.geocode.placeId` | string |  |
| `result.geocode.placeTypes[]` | string |  |

## Native endpoint

Through the native Google Maps API, this operation is `POST https://addressvalidation.googleapis.com/v1::validateAddress?alt=json&fields=*`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-address.md) for the provider-specific parameters and requirements.

