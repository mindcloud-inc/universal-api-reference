# Loqate: Geocode International Location

Geocodes an international location with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/geocode-international-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/geocode-international-location?connectionId=$CONNECTION_ID&country=string&location=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "location": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/geocode-international-location?${params}`, {
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
| `country` | string | yes | The country to search in. |
| `location` | string | yes | The location to geocode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Geocoding/International/Geocode/v1.10/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geocode-international-location.md) for the provider-specific parameters and requirements.

