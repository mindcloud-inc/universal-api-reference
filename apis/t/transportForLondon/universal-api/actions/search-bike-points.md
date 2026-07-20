# Transport for London: Search Bike Points

Finds bike points in Transport for London by name.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-bike-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-bike-points?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/search-bike-points?${params}`, {
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
| `query` | string | yes | Bike point search text, such as street or landmark name. |

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

Through the native Transport for London API, this operation is `GET /BikePoint/Search` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-bike-points.md) for the provider-specific parameters and requirements.

