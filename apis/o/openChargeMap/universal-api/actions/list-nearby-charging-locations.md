# Open Charge Map: List Nearby Charging Locations



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-nearby-charging-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-nearby-charging-locations?connectionId=$CONNECTION_ID&latitude=37.7749&longitude=-122.4194&distance=10&distanceUnit=Miles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "37.7749",
  "longitude": "-122.4194",
  "distance": "10",
  "distanceUnit": "Miles"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-nearby-charging-locations?${params}`, {
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
| `latitude` | number | yes | Latitude for distance calculation and filtering. Default: `37.7749`. Example: `37.7749`. |
| `longitude` | number | yes | Longitude for distance calculation and filtering. Default: `-122.4194`. Example: `-122.4194`. |
| `distance` | number | yes | Maximum distance from the latitude/longitude. Default: `10`. Example: `10`. |
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
| `AddressInfo` | object | Charging location address and coordinates. |
| `Connections` | array<object> | Available charging connections. |
| `DateLastStatusUpdate` | date | Last status update timestamp. |
| `ID` | number | Open Charge Map POI ID. |
| `OperatorInfo` | object | Charging location operator details. |
| `StatusType` | object | Operational status metadata. |
| `UUID` | string | Open Charge Map POI UUID. |

## Native endpoint

Through the native Open Charge Map API, this operation is `GET /poi` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nearby-charging-locations.md) for the provider-specific parameters and requirements.

