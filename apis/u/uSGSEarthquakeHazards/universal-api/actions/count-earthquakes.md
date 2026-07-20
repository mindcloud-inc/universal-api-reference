# USGS Earthquake Hazards: Count Earthquakes

Counts earthquakes matching a USGS Earthquake Hazards query.

```
GET https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/count-earthquakes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USGS Earthquake Hazards `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/count-earthquakes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/count-earthquakes?${params}`, {
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
| `starttime` | string | no | Only count events on or after this ISO8601 UTC time. Example: `2026-05-01T00:00:00Z`. |
| `endtime` | string | no | Only count events on or before this ISO8601 UTC time. Example: `2026-05-04T00:00:00Z`. |
| `minmagnitude` | number | no | Only count events with magnitude greater than or equal to this value. Example: `2.5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "maxAllowed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of catalog events matching the query. |
| `maxAllowed` | number | Maximum number of events USGS allows for the matching query. |

## Native endpoint

Through the native USGS Earthquake Hazards API, this operation is `GET /fdsnws/event/1/count` (base URL `https://earthquake.usgs.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-earthquakes.md) for the provider-specific parameters and requirements.

