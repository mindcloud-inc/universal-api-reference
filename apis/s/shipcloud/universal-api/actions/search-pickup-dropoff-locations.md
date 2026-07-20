# Shipcloud: Search Pickup Dropoff Locations

Finds pickup dropoff locations in Shipcloud.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/search-pickup-dropoff-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/search-pickup-dropoff-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/search-pickup-dropoff-locations?${params}`, {
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
| `carriers` | string | no | Restrict the search to one or more carriers. |
| `city` | string | no | City for address-based pickup/dropoff search. |
| `country` | string | no | ISO country code for address-based pickup/dropoff search. |
| `latitude` | number | no | Latitude for coordinate-based pickup/dropoff search. |
| `limit` | number | no | Maximum number of pickup/dropoff locations to return. |
| `longitude` | number | no | Longitude for coordinate-based pickup/dropoff search. |
| `radius` | number | no | Search radius around the coordinates. |
| `state` | string | no | State or region for address-based pickup/dropoff search. |
| `street` | string | no | Street for address-based pickup/dropoff search. |
| `zipCode` | string | no | ZIP or postal code for address-based pickup/dropoff search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier_code": "string",
      "city": "string",
      "country_code": "string",
      "distance": 1,
      "distance_unit_of_measure": "string",
      "house_number": "string",
      "latitude": 1,
      "longitude": 1,
      "name1": "Ava Chen",
      "pudo_additional_properties": [
        {}
      ],
      "pudo_hours": [
        {}
      ],
      "pudo_measurements": [
        {}
      ],
      "service_point_id": "string",
      "street1": "string",
      "telephone_number": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier_code` | string |  |
| `city` | string |  |
| `country_code` | string |  |
| `distance` | number |  |
| `distance_unit_of_measure` | string |  |
| `house_number` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name1` | string |  |
| `pudo_additional_properties` | array<object> |  |
| `pudo_hours` | array<object> |  |
| `pudo_measurements` | array<object> |  |
| `service_point_id` | string |  |
| `street1` | string |  |
| `telephone_number` | string |  |
| `zip_code` | string |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /pickup_dropoff_locations` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pickup-dropoff-locations.md) for the provider-specific parameters and requirements.

