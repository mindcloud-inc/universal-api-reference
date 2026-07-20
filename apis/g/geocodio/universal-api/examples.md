# Geocodio Universal API Examples

These examples use the MindCloud API key and Geocodio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Geocode Address

Retrieves geocoding results from Geocodio for one address.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/geocode-address?connectionId=$CONNECTION_ID&q=1109%20N%20Highland%20St%2C%20Arlington%20VA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "1109 N Highland St, Arlington VA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/geocode-address?${params}`, {
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
      "input": {
        "addressComponents": {},
        "formattedAddress": "string"
      },
      "results": [
        {
          "accuracy": 1,
          "accuracyType": "string",
          "formattedAddress": "string",
          "location": {
            "lat": 1,
            "lng": 1
          },
          "matchType": "string",
          "source": "string",
          "stableAddressKey": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Geocode Address action reference](actions/geocode-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/geocodio/latest/actions/geocode-address).

## Create Distance Job

Creates an asynchronous distance job in Geocodio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/create-distance-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Store to customer distances",
  "origins[]": "38.8977,-77.0365,WhiteHouse",
  "destinations[]": "38.8895,-77.0353,WashingtonMonument"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/create-distance-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Store to customer distances",
    "origins[]": "38.8977,-77.0365,WhiteHouse",
    "destinations[]": "38.8895,-77.0353,WashingtonMonument"
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
      "calculationsCompleted": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "destinationsCount": 1,
      "destinationsType": "string",
      "distanceMode": "string",
      "downloadUrl": "https://example.com",
      "identifier": "string",
      "isExpired": true,
      "name": "Ava Chen",
      "originsCount": 1,
      "originsType": "string",
      "progress": 1,
      "status": "string",
      "statusMessage": "string",
      "timeLeft": "string",
      "totalCalculations": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Distance Job action reference](actions/create-distance-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/geocodio/latest/actions/create-distance-job).
