# Open Brewery DB: Get Brewery

Retrieves a brewery from Open Brewery DB.

```
GET https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/get-brewery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Brewery DB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/get-brewery?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/get-brewery?${params}`, {
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
| `id` | string | yes | Unique Open Brewery DB brewery identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_1": "string",
      "address_2": "string",
      "address_3": "string",
      "brewery_type": "string",
      "city": "string",
      "country": "string",
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "phone": "string",
      "postal_code": "string",
      "state": "string",
      "state_province": "string",
      "street": "string",
      "website_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_1` | string | Primary street address. |
| `address_2` | string | Secondary address line. |
| `address_3` | string | Third address line. |
| `brewery_type` | string | Type of brewery. |
| `city` | string | City name. |
| `country` | string | Country name. |
| `id` | string | Unique identifier for the brewery. |
| `latitude` | number | Latitude coordinate. |
| `longitude` | number | Longitude coordinate. |
| `name` | string | Brewery name. |
| `phone` | string | Contact phone number. |
| `postal_code` | string | Postal or ZIP code. |
| `state` | string | Deprecated state value. |
| `state_province` | string | State or province. |
| `street` | string | Deprecated street address value. |
| `website_url` | string | Brewery website URL. |

## Native endpoint

Through the native Open Brewery DB API, this operation is `GET /breweries/:id` (base URL `https://api.openbrewerydb.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brewery.md) for the provider-specific parameters and requirements.

