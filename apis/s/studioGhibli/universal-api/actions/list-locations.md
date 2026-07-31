# Studio Ghibli: List Locations



```
GET https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Studio Ghibli `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/list-locations?${params}`, {
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
| `fields` | string | no | Optional comma-separated list of response fields documented by the provider. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "climate": "string",
      "films": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "residents": [
        "string"
      ],
      "surface_water": "string",
      "terrain": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `climate` | string | Climate. |
| `films` | array<string> | Related film URLs. |
| `id` | string | Provider UUID. |
| `name` | string | Location name. |
| `residents` | array<string> | Related person URLs. |
| `surface_water` | string | Native surface-water value. |
| `terrain` | string | Terrain. |
| `url` | string | Canonical resource URL. |

## Native endpoint

Through the native Studio Ghibli API, this operation is `GET /locations` (base URL `https://ghibliapi.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

