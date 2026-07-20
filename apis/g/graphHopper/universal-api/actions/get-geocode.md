# GraphHopper: Geocode Location

Retrieves geocoding results for a query in GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-geocode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-geocode?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-geocode?${params}`, {
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
| `query` | string | no | Address or place text to geocode. Default: `Berlin`. |
| `point` | string | no | Latitude,longitude point for reverse geocoding. |
| `reverse` | boolean | no | Whether to reverse geocode the supplied point. |
| `limit` | number | no | Maximum number of geocoding results to return. |
| `locale` | string | no | Locale of returned names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hits": [
        {}
      ],
      "locale": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hits` | array<object> | Geocoding hits. |
| `locale` | string | Locale used for the geocoding response. |

## Native endpoint

Through the native GraphHopper API, this operation is `GET /geocode` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-geocode.md) for the provider-specific parameters and requirements.

