# Chicago Transit Authority: Get Train Arrivals by Station

Retrieves train arrival predictions in Chicago Transit Authority by station.

```
GET https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chicago Transit Authority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station?connectionId=$CONNECTION_ID&mapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station?${params}`, {
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
| `mapId` | string | yes | CTA station map ID from the Train Tracker docs, such as 40380 for Clark/Lake. |
| `route` | list | no | Optional CTA rail route code such as Red, Blue, Brn, Org, Pnk, G, or Y. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `max` | number | no | Optional maximum number of arrivals to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arrT": "2026-05-07T12:00:00.000Z",
      "destNm": "string",
      "destSt": "string",
      "heading": "string",
      "isApp": true,
      "isDly": true,
      "isFlt": true,
      "isSch": true,
      "lat": "string",
      "lon": "string",
      "prdt": "2026-05-07T12:00:00.000Z",
      "rn": "string",
      "rt": "string",
      "staId": "string",
      "staNm": "string",
      "stpDe": "string",
      "stpId": "string",
      "trDr": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arrT` | date | Arrival timestamp. |
| `destNm` | string | Destination station name. |
| `destSt` | string | Destination station ID. |
| `heading` | string | Train heading in degrees. |
| `isApp` | boolean | Whether the arrival is approaching. |
| `isDly` | boolean | Whether the train is delayed. |
| `isFlt` | boolean | Whether the train is following another train. |
| `isSch` | boolean | Whether the arrival is scheduled. |
| `lat` | string | Train latitude. |
| `lon` | string | Train longitude. |
| `prdt` | date | Prediction timestamp. |
| `rn` | string | Train run number. |
| `rt` | string | CTA rail route code. |
| `staId` | string | CTA station map ID. |
| `staNm` | string | Station name. |
| `stpDe` | string | Platform description. |
| `stpId` | string | CTA platform stop ID. |
| `trDr` | string | Travel direction code. |

## Native endpoint

Through the native Chicago Transit Authority API, this operation is `GET /ttarrivals.aspx` (base URL `https://lapi.transitchicago.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-train-arrivals-by-station.md) for the provider-specific parameters and requirements.

