# Geoapify Geocode Universal API Examples

These examples use the MindCloud API key and Geoapify Geocode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Forward Geocoding

Finds locations in Geoapify by address.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/forward-geocoding?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/forward-geocoding?${params}`, {
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
      "bbox": [
        1
      ],
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "properties": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "Ava Chen",
        "country": "string",
        "countryCode": "string",
        "datasource": {
          "attribution": "string",
          "license": "string",
          "sourcename": "Ava Chen",
          "url": "https://example.com"
        },
        "district": "string",
        "formatted": "string",
        "housenumber": "string",
        "iso31662": "string",
        "lat": 1,
        "lon": 1,
        "name": "Ava Chen",
        "placeId": "string",
        "plusCode": "string",
        "postcode": "string",
        "rank": {
          "confidence": 1,
          "confidenceBuildingLevel": 1,
          "confidenceCityLevel": 1,
          "confidenceStreetLevel": 1,
          "importance": 1,
          "matchType": "string",
          "popularity": 1
        },
        "resultType": "string",
        "state": "string",
        "stateCode": "string",
        "street": "Ava Chen",
        "suburb": "string",
        "timezone": {
          "abbreviationDST": "string",
          "abbreviationSTD": "string",
          "name": "Ava Chen",
          "offsetDST": "string",
          "offsetDSTSeconds": 1,
          "offsetSTD": "string",
          "offsetSTDSeconds": 1
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Forward Geocoding action reference](actions/forward-geocoding.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/geoapify/latest/actions/forward-geocoding).
