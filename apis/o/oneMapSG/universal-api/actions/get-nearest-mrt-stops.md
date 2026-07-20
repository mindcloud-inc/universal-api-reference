# OneMap SG: Get Nearest MRT Stops

Retrieves nearest MRT stops from OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-nearest-mrt-stops
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-nearest-mrt-stops?connectionId=$CONNECTION_ID&latitude=1.4044693603639506&longitude=103.90083627504391" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1.4044693603639506",
  "longitude": "103.90083627504391"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-nearest-mrt-stops?${params}`, {
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
| `latitude` | number | yes | The latitude to search nearby MRT stops around. Example: `1.4044693603639506`. |
| `longitude` | number | yes | The longitude to search nearby MRT stops around. Example: `103.90083627504391`. |
| `radiusInMeters` | number | no | The search radius in meters. Default: `1000`. Example: `1000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "lat": 1,
      "lon": 1,
      "name": "Ava Chen",
      "road": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The stop identifier. |
| `lat` | number | The stop latitude. |
| `lon` | number | The stop longitude. |
| `name` | string | The stop name. |
| `road` | string | The nearby road name. |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/nearbysvc/getNearestMrtStops` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-nearest-mrt-stops.md) for the provider-specific parameters and requirements.

