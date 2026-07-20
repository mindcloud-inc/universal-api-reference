# NiftyImages: Search Map Locations By Address

Finds map locations in NiftyImages by address.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/search-map-locations-by-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/search-map-locations-by-address?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/search-map-locations-by-address?${params}`, {
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
| `url` | string | yes | NiftyImages map URL. |
| `address` | string | yes | Address to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": "string",
      "Latitude": 1,
      "LocationID": "string",
      "Longitude": 1,
      "NiftyID": "string",
      "Properties": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address` | string |  |
| `Latitude` | number |  |
| `LocationID` | string |  |
| `Longitude` | number |  |
| `NiftyID` | string |  |
| `Properties[]` | array<object> |  |
| `Properties[].Name` | string |  |
| `Properties[].Value` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /Maps/GetLocations` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-map-locations-by-address.md) for the provider-specific parameters and requirements.

