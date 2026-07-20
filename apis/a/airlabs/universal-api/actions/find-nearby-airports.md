# Airlabs: Find Nearby Airports

Finds nearby airports in Airlabs by coordinates.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/find-nearby-airports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/find-nearby-airports?connectionId=$CONNECTION_ID&lat=1&lng=1&distance=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lng": "1",
  "distance": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/find-nearby-airports?${params}`, {
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
| `lat` | number | yes | Geo-location latitude. |
| `lng` | number | yes | Geo-location longitude. |
| `distance` | number | yes | Distance from the location in kilometers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airports": [
        {}
      ],
      "cities": [
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
| `airports` | array<object> | Nearby airports. |
| `cities` | array<object> | Nearby cities. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /nearby` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-nearby-airports.md) for the provider-specific parameters and requirements.

