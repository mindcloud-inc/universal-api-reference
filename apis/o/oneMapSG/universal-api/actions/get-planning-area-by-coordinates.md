# OneMap SG: Get Planning Area by Coordinates

Retrieves a planning area from OneMap SG by coordinates.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-planning-area-by-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-planning-area-by-coordinates?connectionId=$CONNECTION_ID&latitude=1.3&longitude=103.8&year=2019" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1.3",
  "longitude": "103.8",
  "year": "2019"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-planning-area-by-coordinates?${params}`, {
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
| `latitude` | number | yes | The latitude to look up the planning area for. Example: `1.3`. |
| `longitude` | number | yes | The longitude to look up the planning area for. Example: `103.8`. |
| `year` | number | yes | The reference year for the planning area lookup. Example: `2019`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "geojson": "string",
      "pln_area_n": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `geojson` | string |  |
| `pln_area_n` | string |  |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/popapi/getPlanningarea` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-planning-area-by-coordinates.md) for the provider-specific parameters and requirements.

