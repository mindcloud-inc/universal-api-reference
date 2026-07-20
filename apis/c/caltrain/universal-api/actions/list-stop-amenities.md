# Caltrain: List Stop Amenities

Retrieves amenities for a Caltrain stop.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-stop-amenities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-stop-amenities?connectionId=$CONNECTION_ID&stopId=70021" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stopId": "70021"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/list-stop-amenities?${params}`, {
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
| `stopId` | string | yes | Caltrain stop identifier such as 70021 or 22nd_street. Example: `70021`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldAmenity": [
        {
          "value": "string"
        }
      ],
      "geodata": [
        {
          "bottom": 1,
          "geohash": "string",
          "geoType": "string",
          "lat": 1,
          "latlon": "string",
          "left": 1,
          "lon": 1,
          "right": 1,
          "top": 1,
          "value": "string"
        }
      ],
      "id": [
        {
          "value": "string"
        }
      ],
      "name": [
        {
          "value": "Ava Chen"
        }
      ],
      "osmEditLink": [
        {
          "uri": "https://example.com"
        }
      ],
      "osmId": [
        {
          "value": "string"
        }
      ],
      "osmViewLink": [
        {
          "uri": "https://example.com"
        }
      ],
      "type": [
        {
          "targetId": "string"
        }
      ],
      "way": [
        {
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldAmenity[].value` | string |  |
| `geodata[].bottom` | number |  |
| `geodata[].geohash` | string |  |
| `geodata[].geoType` | string |  |
| `geodata[].lat` | number |  |
| `geodata[].latlon` | string |  |
| `geodata[].left` | number |  |
| `geodata[].lon` | number |  |
| `geodata[].right` | number |  |
| `geodata[].top` | number |  |
| `geodata[].value` | string |  |
| `id[].value` | string |  |
| `name[].value` | string |  |
| `osmEditLink[].uri` | string |  |
| `osmId[].value` | string |  |
| `osmViewLink[].uri` | string |  |
| `type[].targetId` | string |  |
| `way[].value` | string |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /gtfs/stops/:stopId/amenities` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stop-amenities.md) for the provider-specific parameters and requirements.

