# Apple Map Links: Frame Map

Frames a map view in Apple Maps.

```
GET https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/frame-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple Map Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/frame-map?connectionId=$CONNECTION_ID&center=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "center": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/frame-map?${params}`, {
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
| `center` | string | yes | Map center as a comma-separated latitude,longitude coordinate pair. |
| `span` | string | no | Visible area span around the center as latitudeDelta,longitudeDelta. |
| `map` | string | no | Map type: explore, driving, transit, satellite, or hybrid. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | string | no | Optional location tracking mode: follow, follow-with-heading, or none. |
| `heading` | number | no | Map camera heading in degrees. |
| `pitch` | number | no | Map camera pitch angle. |
| `distance` | number | no | Apparent distance from the viewer to the map surface. |

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

Through the native Apple Map Links API, this operation is `GET /frame` (base URL `https://maps.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/frame-map.md) for the provider-specific parameters and requirements.

