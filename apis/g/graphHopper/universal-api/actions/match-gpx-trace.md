# GraphHopper: Match GPX Trace

Matches a GPX trace in GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/match-gpx-trace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/match-gpx-trace?connectionId=$CONNECTION_ID&gpx=string&profile=car" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "gpx": "string",
  "profile": "car"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/match-gpx-trace?${params}`, {
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
| `gpx` | string | yes | GPX XML content to map-match. |
| `profile` | string | yes | Routing profile for map matching. Default: `car`. |
| `gpsAccuracy` | number | no | GPS accuracy in meters. |
| `locale` | string | no | Locale of instructions. Default: `en`. |
| `instructions` | boolean | no | Whether turn-by-turn instructions should be calculated. |
| `pointsEncoded` | boolean | no | Whether returned geometry should use encoded polyline format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": {},
      "paths": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | object | Response metadata. |
| `paths` | array<object> | Matched route paths. |

## Native endpoint

Through the native GraphHopper API, this operation is `POST /match` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/match-gpx-trace.md) for the provider-specific parameters and requirements.

