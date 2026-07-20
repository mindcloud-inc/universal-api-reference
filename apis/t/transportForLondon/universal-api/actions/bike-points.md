# Transport for London: List Bike Points

Retrieves bike points from Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/bike-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/bike-points?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/bike-points?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalProperties": [
        {}
      ],
      "commonName": "Ava Chen",
      "id": "string",
      "lat": 1,
      "lon": 1,
      "placeType": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalProperties` | array<object> |  |
| `commonName` | string |  |
| `id` | string |  |
| `lat` | number |  |
| `lon` | number |  |
| `placeType` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /BikePoint` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bike-points.md) for the provider-specific parameters and requirements.

