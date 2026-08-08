# Google Maps: Get Route Matrix



```
GET https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/get-route-matrix
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Maps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/get-route-matrix?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/get-route-matrix?${params}`, {
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
| `destinations[].longitude` | number | no |  |
| `destinations[].latitude` | number | no |  |
| `origins[].latitude` | number | no |  |
| `origins[].routeModifiers.avoidTolls` | boolean | no |  |
| `origins[]` | array | no |  |
| `origins[].longitude` | number | no |  |
| `origins[].routeModifiers.avoidHighways` | boolean | no |  |
| `destinations[]` | array | no |  |
| `origins[].routeModifiers` | object | no |  |
| `origins[].routeModifiers.avoidFerries` | boolean | no |  |
| `origins[].routeModifiers.avoidIndoor` | boolean | no |  |
| `routingPreference` | list | no |  |
| `travelMode` | list | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "condition": "string",
      "destinationIndex": 1,
      "distanceMeters": 1,
      "duration": "string",
      "originIndex": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `condition` | string |  |
| `destinationIndex` | number |  |
| `distanceMeters` | number |  |
| `duration` | string |  |
| `originIndex` | number |  |

## Native endpoint

Through the native Google Maps API, this operation is `POST https://routes.googleapis.com/distanceMatrix/v2:computeRouteMatrix`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-route-matrix.md) for the provider-specific parameters and requirements.

