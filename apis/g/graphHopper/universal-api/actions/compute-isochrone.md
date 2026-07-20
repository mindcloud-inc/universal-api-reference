# GraphHopper: Compute Isochrone

Computes an isochrone map in GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/compute-isochrone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/compute-isochrone?connectionId=$CONNECTION_ID&point=string&profile=car" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "point": "string",
  "profile": "car"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/compute-isochrone?${params}`, {
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
| `point` | string | yes | Center point as `lat,lon`. |
| `profile` | string | yes | Routing profile such as `car`, `bike`, or `foot`. Default: `car`. |
| `timeLimit` | number | no | Travel time limit in seconds. |
| `distanceLimit` | number | no | Travel distance limit in meters. |
| `buckets` | number | no | Number of isochrone buckets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "polygons": [
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
| `polygons` | array<object> | Isochrone polygons. |

## Native endpoint

Through the native GraphHopper API, this operation is `GET /isochrone` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compute-isochrone.md) for the provider-specific parameters and requirements.

