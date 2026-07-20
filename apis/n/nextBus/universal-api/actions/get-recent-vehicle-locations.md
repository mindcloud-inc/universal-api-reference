# NextBus: Get Recent Vehicle Locations

Retrieves recent vehicle locations from NextBus.

```
GET https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-recent-vehicle-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-recent-vehicle-locations?connectionId=$CONNECTION_ID&agencyTag=glendale&routeTag=01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agencyTag": "glendale",
  "routeTag": "01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-recent-vehicle-locations?${params}`, {
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
| `agencyTag` | string | yes | Default: `glendale`. |
| `routeTag` | string | yes | Default: `01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dirTag": "string",
      "heading": "string",
      "id": "string",
      "lat": "string",
      "lon": "string",
      "predictable": "string",
      "routeTag": "string",
      "secsSinceReport": "string",
      "speedKmHr": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dirTag` | string |  |
| `heading` | string |  |
| `id` | string |  |
| `lat` | string |  |
| `lon` | string |  |
| `predictable` | string |  |
| `routeTag` | string |  |
| `secsSinceReport` | string |  |
| `speedKmHr` | string |  |

## Native endpoint

Through the native NextBus API, this operation is `GET /publicXMLFeed` (base URL `https://retro.umoiq.com/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recent-vehicle-locations.md) for the provider-specific parameters and requirements.

