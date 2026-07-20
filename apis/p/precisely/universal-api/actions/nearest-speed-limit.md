# Precisely: Nearest Speed Limit

Retrieves the nearest speed limit from Precisely by location.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearest-speed-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearest-speed-limit?connectionId=$CONNECTION_ID&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearest-speed-limit?${params}`, {
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
| `path` | string | yes | Two to five semicolon-separated longitude,latitude coordinate pairs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amPeakAvgSpeed": "string",
      "maxSpeed": "string",
      "nightAvgSpeed": "string",
      "offPeakAvgSpeed": "string",
      "pmPeakAvgSpeed": "string",
      "road": {
        "id": "string",
        "isToll": "string",
        "lengthInMeters": "string",
        "name": "Ava Chen",
        "roadClass": "string",
        "surfaceType": "string",
        "trafficFlow": "string",
        "type": "string"
      },
      "speedUnit": "string",
      "speedVerification": "string",
      "weekAvgSpeed": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amPeakAvgSpeed` | string | Average observed speed during the morning peak period. |
| `maxSpeed` | string | Posted maximum speed limit for the matched road segment. |
| `nightAvgSpeed` | string | Average observed speed during night hours. |
| `offPeakAvgSpeed` | string | Average observed speed during off-peak periods. |
| `pmPeakAvgSpeed` | string | Average observed speed during the evening peak period. |
| `road.id` | string | Provider identifier for the matched road segment. |
| `road.isToll` | string | Whether the matched road segment is a toll road. |
| `road.lengthInMeters` | string | Length of the matched road segment in meters. |
| `road.name` | string | Matched road name. |
| `road.roadClass` | string | Road-class label for the matched segment. |
| `road.surfaceType` | string | Surface type for the matched road segment. |
| `road.trafficFlow` | string | Traffic-flow direction reported for the matched segment. |
| `road.type` | string | Road carriageway type. |
| `speedUnit` | string | Unit used for the reported speed limit. |
| `speedVerification` | string | Provider verification status for the speed limit. |
| `weekAvgSpeed` | string | Average observed speed across the week. |

## Native endpoint

Through the native Precisely API, this operation is `GET /streets/v1/speedlimit` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nearest-speed-limit.md) for the provider-specific parameters and requirements.

