# Google Maps: Geocode Address



```
GET https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/geocode-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Maps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/geocode-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/geocode-address?${params}`, {
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
| `address` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "addressComponents": [
            {
              "longName": "Ava Chen",
              "shortName": "Ava Chen",
              "types": [
                "string"
              ]
            }
          ],
          "formattedAddress": "string",
          "geometry": {
            "bounds": {
              "northeast": {
                "lat": 1,
                "lng": 1
              },
              "southwest": {
                "lat": 1,
                "lng": 1
              }
            },
            "location": {
              "lat": 1,
              "lng": 1
            },
            "locationType": "string",
            "viewport": {
              "northeast": {
                "lat": 1,
                "lng": 1
              },
              "southwest": {
                "lat": 1,
                "lng": 1
              }
            }
          },
          "navigationPoints": [
            {
              "location": {
                "latitude": 1,
                "longitude": 1
              }
            }
          ],
          "placeId": "string",
          "types": [
            "string"
          ]
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].addressComponents[].longName` | string |  |
| `results[].addressComponents[].shortName` | string |  |
| `results[].addressComponents[].types[]` | string |  |
| `results[].formattedAddress` | string |  |
| `results[].geometry.bounds.northeast.lat` | number |  |
| `results[].geometry.bounds.northeast.lng` | number |  |
| `results[].geometry.bounds.southwest.lat` | number |  |
| `results[].geometry.bounds.southwest.lng` | number |  |
| `results[].geometry.location.lat` | number |  |
| `results[].geometry.location.lng` | number |  |
| `results[].geometry.locationType` | string |  |
| `results[].geometry.viewport.northeast.lat` | number |  |
| `results[].geometry.viewport.northeast.lng` | number |  |
| `results[].geometry.viewport.southwest.lat` | number |  |
| `results[].geometry.viewport.southwest.lng` | number |  |
| `results[].navigationPoints[].location.latitude` | number |  |
| `results[].navigationPoints[].location.longitude` | number |  |
| `results[].placeId` | string |  |
| `results[].types[]` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Google Maps API, this operation is `GET https://maps.googleapis.com/maps/api/geocode/json`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geocode-address.md) for the provider-specific parameters and requirements.

