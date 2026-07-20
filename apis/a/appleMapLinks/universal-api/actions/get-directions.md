# Apple Map Links: Get Directions

Opens Apple Maps directions between locations.

```
GET https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/get-directions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple Map Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/get-directions?connectionId=$CONNECTION_ID&destination=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "destination": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/get-directions?${params}`, {
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
| `source` | string | no | Optional starting point as an address, coordinate, or place name. |
| `destination` | string | yes | Ending destination as an address, coordinate, or place name. |
| `waypoint` | string | no | Optional intermediate stop. Apple Maps allows repeating this query parameter for multistop routing. |
| `mode` | string | no | Transportation mode: driving, walking, transit, or cycling. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourcePlaceId` | string | no | Optional Place ID for the source; requires source. |
| `destinationPlaceId` | string | no | Optional Place ID for the destination; requires destination. |
| `waypointPlaceId` | string | no | Optional Place ID for a waypoint. |
| `avoid` | string | no | Comma-delimited route avoid preferences, such as tolls, highways, busy-roads, or stairs. |
| `transitPreferences` | string | no | Comma-delimited transit preferences: bus, subway, commuter, or ferry. |
| `start` | number | no | Delay in seconds before starting navigation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Generated Apple Maps URL. |

## Native endpoint

Through the native Apple Map Links API, this operation is `GET /directions` (base URL `https://maps.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-directions.md) for the provider-specific parameters and requirements.

