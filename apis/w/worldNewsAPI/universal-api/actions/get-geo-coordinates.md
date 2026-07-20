# World News API: Get Geo Coordinates

Retrieves geo coordinates for a location from World News API.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/get-geo-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/get-geo-coordinates?connectionId=$CONNECTION_ID&location=Buenos%20Aires%2C%20Argentina" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "Buenos Aires, Argentina"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/get-geo-coordinates?${params}`, {
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
| `location` | string | yes | Location string to geocode into latitude and longitude. Default: `Buenos Aires, Argentina`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "latitude": 1,
      "longitude": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | Resolved city name when available. |
| `latitude` | number | Latitude of the resolved location. |
| `longitude` | number | Longitude of the resolved location. |

## Native endpoint

Through the native World News API API, this operation is `GET /geo-coordinates` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-geo-coordinates.md) for the provider-specific parameters and requirements.

