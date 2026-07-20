# Caltrain: Search Amenities

Finds Caltrain amenities within map bounds.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/search-amenities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/search-amenities?connectionId=$CONNECTION_ID&west=-122.40&south=37.75&east=-122.38&north=37.77" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "west": "-122.40",
  "south": "37.75",
  "east": "-122.38",
  "north": "37.77"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/search-amenities?${params}`, {
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
| `west` | number | yes | West longitude bound. Example: `-122.40`. |
| `south` | number | yes | South latitude bound. Example: `37.75`. |
| `east` | number | yes | East longitude bound. Example: `-122.38`. |
| `north` | number | yes | North latitude bound. Example: `37.77`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_amenity": [
        {}
      ],
      "field_website": [
        {}
      ],
      "geodata": [
        {}
      ],
      "id": [
        {}
      ],
      "name": [
        {}
      ],
      "osm_id": [
        {}
      ],
      "type": [
        {}
      ],
      "way": [
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
| `field_amenity` | array<object> |  |
| `field_website` | array<object> |  |
| `geodata` | array<object> |  |
| `id` | array<object> |  |
| `name` | array<object> |  |
| `osm_id` | array<object> |  |
| `type` | array<object> |  |
| `way` | array<object> |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /search/amenities/:west,:south,:east,:north` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-amenities.md) for the provider-specific parameters and requirements.

