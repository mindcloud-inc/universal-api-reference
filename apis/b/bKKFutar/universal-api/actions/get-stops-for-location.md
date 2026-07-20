# BKK Futar: Get Stops For Location

Retrieves stops for a selected location, or all stops, in BKK Futar.

```
GET https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-stops-for-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BKK Futar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-stops-for-location?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-stops-for-location?${params}`, {
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
| `lat` | number | no | Latitude of the requested location. |
| `lon` | number | no | Longitude of the requested location. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lat_span` | number | no | Latitude span around the requested location. |
| `lon_span` | number | no | Longitude span around the requested location. |
| `radius` | number | no | Search radius in meters when spans are omitted. |
| `min_result` | number | no | Minimum number of elements returned. |
| `include_references` | string | no | Reference data to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limitExceeded": true,
      "list": {
        "alertIds": [
          "string"
        ],
        "code": "string",
        "description": "string",
        "direction": "string",
        "id": "string",
        "lat": 1,
        "locationSubType": "string",
        "locationType": 1,
        "lon": 1,
        "name": "Ava Chen",
        "parentStationId": "string",
        "platformCode": "string",
        "routeIds": [
          "string"
        ],
        "vertex": "string",
        "wheelchairBoarding": true
      },
      "references": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limitExceeded` | boolean | Whether the response exceeded the defined limit. |
| `list` | array<object> | Stops returned for the requested location. |
| `list.alertIds` | array<string> | Active alert IDs related to the stop. |
| `list.code` | string | Stop code. |
| `list.description` | string | Stop description. |
| `list.direction` | string | Stop direction. |
| `list.id` | string | Unique stop ID. |
| `list.lat` | number | Stop latitude. |
| `list.locationSubType` | string | Stop location subtype. |
| `list.locationType` | number | Stop location type. |
| `list.lon` | number | Stop longitude. |
| `list.name` | string | Stop name. |
| `list.parentStationId` | string | Parent station ID. |
| `list.platformCode` | string | Platform code. |
| `list.routeIds` | array<string> | Routes containing the stop. |
| `list.vertex` | string | Journey planner stop identifier. |
| `list.wheelchairBoarding` | boolean | Whether the stop is wheelchair accessible. |
| `references` | object | Included reference details. |

## Native endpoint

Through the native BKK Futar API, this operation is `GET /stops-for-location.json` (base URL `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stops-for-location.md) for the provider-specific parameters and requirements.

