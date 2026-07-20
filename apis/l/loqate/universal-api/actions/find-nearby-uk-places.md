# Loqate: Find Nearby UK Places

Finds nearby UK places with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-nearby-uk-places
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-nearby-uk-places?connectionId=$CONNECTION_ID&centrePoint=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "centrePoint": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-nearby-uk-places?${params}`, {
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
| `centrePoint` | string | yes | The centre point for the UK search. |
| `maximumItems` | number | no | Maximum number of places to return. |
| `maximumRadius` | number | no | Maximum radius in KM for the search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "distance": 1,
      "easting": 1,
      "latitude": 1,
      "longitude": 1,
      "northing": 1,
      "osGrid": "string",
      "postcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `distance` | number |  |
| `easting` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `northing` | number |  |
| `osGrid` | string |  |
| `postcode` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Geocoding/UK/RetrieveNearestPlaces/v1.20/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-nearby-uk-places.md) for the provider-specific parameters and requirements.

