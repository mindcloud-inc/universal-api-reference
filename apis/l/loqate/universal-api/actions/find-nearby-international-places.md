# Loqate: Find Nearby International Places

Finds nearby international places with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-nearby-international-places
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-nearby-international-places?connectionId=$CONNECTION_ID&centrePoint=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "centrePoint": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-nearby-international-places?${params}`, {
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
| `centrePoint` | string | yes | The centre point for the search. |
| `country` | string | no | Optional ISO3 country code for place-name searches. |
| `maximumItems` | number | no | Maximum number of places to return. |
| `maximumRadius` | number | no | Maximum radius in KM for the search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "distance": 1,
      "latitude": 1,
      "location": "string",
      "longitude": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `distance` | number |  |
| `latitude` | number |  |
| `location` | string |  |
| `longitude` | number |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Geocoding/International/RetrieveNearestPlaces/v1.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-nearby-international-places.md) for the provider-specific parameters and requirements.

