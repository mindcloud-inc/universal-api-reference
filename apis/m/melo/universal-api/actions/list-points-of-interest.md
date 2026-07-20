# Melo: List Points of Interest

Retrieves points of interest from Melo near specific coordinates.

```
GET https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-points-of-interest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Melo `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-points-of-interest?connectionId=$CONNECTION_ID&lat=1&lon=1&facilities=school%2Ckindergarten" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1",
  "facilities": "school,kindergarten"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-points-of-interest?${params}`, {
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
| `lat` | number | yes | Latitude coordinate. |
| `lon` | number | yes | Longitude coordinate. |
| `radius` | number | no | Search radius in kilometers. Default: `3`. |
| `facilities` | string<string> | yes | Facility types to include, comma-separated (for example school,kindergarten,bus_stop). Example: `school,kindergarten`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "lat": 1,
      "lon": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `lat` | number |  |
| `lon` | number |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Melo API, this operation is `GET /indicators/points_of_interest` (base URL `https://preprod-api.notif.immo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-points-of-interest.md) for the provider-specific parameters and requirements.

