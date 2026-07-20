# Open Charge Map: List Charging Locations Along Route



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-along-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-along-route?connectionId=$CONNECTION_ID&polyline=c%7CpeFf%60ejVo%7D%40o%7D%40&distance=1&distanceUnit=Miles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "polyline": "c|peFf`ejVo}@o}@",
  "distance": "1",
  "distanceUnit": "Miles"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-along-route?${params}`, {
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
| `polyline` | string | yes | Encoded route polyline. Use with distance to search along a route. Default: `c\|peFf`ejVo}@o}@`. Example: `c\|peFf`ejVo}@o}@`. |
| `distance` | number | yes | Search distance around the route polyline. Default: `1`. Example: `1`. |
| `distanceUnit` | list | yes | Distance unit: miles or km. One of: `0`, `1`. Default: `Miles`. Example: `Miles`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AddressInfo": {},
      "Connections": [
        {}
      ],
      "DateLastStatusUpdate": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "OperatorInfo": {},
      "StatusType": {},
      "UUID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AddressInfo` | object |  |
| `Connections` | array<object> |  |
| `DateLastStatusUpdate` | date |  |
| `ID` | number |  |
| `OperatorInfo` | object |  |
| `StatusType` | object |  |
| `UUID` | string |  |

## Native endpoint

Through the native Open Charge Map API, this operation is `GET /poi` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-charging-locations-along-route.md) for the provider-specific parameters and requirements.

