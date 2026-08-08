# Google Maps Universal API Examples

These examples use the MindCloud API key and Google Maps connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Geocode Address



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

Example response:

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

See the full [Geocode Address action reference](actions/geocode-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleMaps/latest/actions/geocode-address).

## Validate Address

Validates an Address

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

Example response:

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

See the full [Validate Address action reference](actions/validate-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleMaps/latest/actions/validate-address).
