# Wasi: Get Property

Retrieves a property from Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-property?connectionId=$CONNECTION_ID&property_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "property_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-property?${params}`, {
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
| `property_id` | number | yes | Wasi property ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "area": 1,
      "bathrooms": 1,
      "bedrooms": 1,
      "built_area": 1,
      "city_label": "string",
      "country_label": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "features": {},
      "floor": "string",
      "for_rent": true,
      "for_sale": true,
      "for_transfer": true,
      "galleries": [
        {}
      ],
      "garages": 1,
      "id_city": 1,
      "id_country": 1,
      "id_location": 1,
      "id_property": 1,
      "id_property_type": 1,
      "id_region": 1,
      "id_user": 1,
      "location_label": "string",
      "main_image": {},
      "observations": "string",
      "property_type_label": "string",
      "region_label": "string",
      "rent_price": 1,
      "sale_price": 1,
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Property address. |
| `area` | number | Property area. |
| `bathrooms` | number | Bathroom count. |
| `bedrooms` | number | Bedroom count. |
| `built_area` | number | Built area. |
| `city_label` | string | City name. |
| `country_label` | string | Country name. |
| `created_at` | date | Creation timestamp. |
| `features` | object | Property features payload. |
| `floor` | string | Floor or level label. |
| `for_rent` | boolean | Whether the property is for rent. |
| `for_sale` | boolean | Whether the property is for sale. |
| `for_transfer` | boolean | Whether the property is for transfer. |
| `galleries` | array<object> | Property gallery groups. |
| `garages` | number | Garage count. |
| `id_city` | number | City identifier. |
| `id_country` | number | Country identifier. |
| `id_location` | number | Locality identifier. |
| `id_property` | number | Wasi property identifier. |
| `id_property_type` | number | Property type identifier. |
| `id_region` | number | Region identifier. |
| `id_user` | number | Assigned Wasi user identifier. |
| `location_label` | string | Locality name. |
| `main_image` | object | Primary property image payload. |
| `observations` | string | Property observations. |
| `property_type_label` | string | Property type label. |
| `region_label` | string | Region name. |
| `rent_price` | number | Rent price. |
| `sale_price` | number | Sale price. |
| `title` | string | Property title. |
| `updated_at` | date | Update timestamp. |

## Native endpoint

Through the native Wasi API, this operation is `GET /property/get/:id_property` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property.md) for the provider-specific parameters and requirements.

