# Onfleet: Get Workers By Location

Finds workers in Onfleet near a location.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-workers-by-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-workers-by-location?connectionId=$CONNECTION_ID&longitude=1&latitude=1&radius=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "longitude": "1",
  "latitude": "1",
  "radius": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-workers-by-location?${params}`, {
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
| `longitude` | number | yes | The longitude component of the coordinate pair. |
| `latitude` | number | yes | The latitude component of the coordinate pair. |
| `radius` | number | yes | The radius around the coordinate pair to search within. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "workers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workers` | array |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /workers/location` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workers-by-location.md) for the provider-specific parameters and requirements.

