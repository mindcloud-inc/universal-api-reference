# OneMap SG: Route (Public Transport)

Retrieves a public transport route from OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-public-transport
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-public-transport?connectionId=$CONNECTION_ID&start=1.320981%2C103.844150&end=1.326762%2C103.8559&date=08-13-2023&time=07%3A35%3A00" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "1.320981,103.844150",
  "end": "1.326762,103.8559",
  "date": "08-13-2023",
  "time": "07:35:00"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/route-public-transport?${params}`, {
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
| `start` | string | yes | The start location as latitude and longitude. Example: `1.320981,103.844150`. |
| `end` | string | yes | The destination location as latitude and longitude. Example: `1.326762,103.8559`. |
| `date` | string | yes | The travel date in MM-DD-YYYY format. Example: `08-13-2023`. |
| `time` | string | yes | The travel time in HH:mm:ss format. Example: `07:35:00`. |
| `maxWalkDistance` | number | no | The maximum walking distance allowed for the route. Default: `1000`. Example: `1000`. |
| `numItineraries` | number | no | The number of itineraries to return. Default: `3`. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "debugOutput": {},
      "elevationMetadata": {},
      "metadata": {},
      "nextPageCursor": "string",
      "plan": {},
      "previousPageCursor": "string",
      "requestParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `debugOutput` | object | The runtime debug information returned by OneMap. |
| `elevationMetadata` | object | Elevation metadata for the route response. |
| `metadata` | object | Additional route metadata such as paging windows. |
| `nextPageCursor` | string | The cursor for the next result page when available. |
| `plan` | object | The transit routing plan returned by OneMap. |
| `previousPageCursor` | string | The cursor for the previous result page when available. |
| `requestParameters` | object | The routing parameters accepted by OneMap for the request. |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/routingsvc/route` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/route-public-transport.md) for the provider-specific parameters and requirements.

