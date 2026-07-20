# Transport for London: Find Nearby Stop Points

Finds nearby stop points in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/nearby-stop-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/nearby-stop-points?connectionId=$CONNECTION_ID&stopTypes=string&locationLat=1&locationLon=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stopTypes": "string",
  "locationLat": "1",
  "locationLon": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/nearby-stop-points?${params}`, {
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
| `stopTypes` | string | yes | Comma-separated stop types to return. Valid values are available from StopPoint/Meta/StopTypes. |
| `locationLat` | number | yes | Latitude for the center of the search. |
| `locationLon` | number | yes | Longitude for the center of the search. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `radius` | number | no | Search radius in metres. TfL defaults this to 200 when omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "centrePoint": [
        1
      ],
      "pageSize": 1,
      "stopPoints": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `centrePoint` | array<number> |  |
| `pageSize` | number |  |
| `stopPoints` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /StopPoint` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nearby-stop-points.md) for the provider-specific parameters and requirements.

