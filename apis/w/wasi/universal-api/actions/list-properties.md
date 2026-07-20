# Wasi: List Properties

Finds properties in Wasi by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-properties?${params}`, {
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
| `match` | string | no | Keywords to search across properties. |
| `country_id` | number | no | Filter by Wasi country identifier. |
| `title` | string | no | Filter by a partial or full property title. |
| `property_id` | number | no | Return a specific property by its Wasi identifier. |
| `region_id` | number | no | Filter by Wasi region identifier. |
| `city_id` | number | no | Filter by Wasi city identifier. |
| `location_id` | number | no | Filter by Wasi location identifier. |
| `property_type_id` | number | no | Filter by Wasi property type identifier. |
| `for_sale` | boolean | no | Only return properties available for sale. |
| `for_rent` | boolean | no | Only return properties available for rent. |
| `for_transfer` | boolean | no | Only return properties available for transfer. |
| `scope` | number | no | Choose whether to include your own properties, allies, all, or group results. |
| `short` | boolean | no | Exclude galleries and features from the response when true. |
| `lax_business_type` | boolean | no | When true, return properties matching any selected business type instead of all selected business types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city_label": "string",
      "country_label": "string",
      "for_rent": true,
      "for_sale": true,
      "for_transfer": true,
      "id_city": 1,
      "id_country": 1,
      "id_property": 1,
      "id_property_type": 1,
      "id_region": 1,
      "property_type_label": "string",
      "region_label": "string",
      "rent_price": 1,
      "sale_price": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Property address. |
| `city_label` | string | City name. |
| `country_label` | string | Country name. |
| `for_rent` | boolean | Whether the property is for rent. |
| `for_sale` | boolean | Whether the property is for sale. |
| `for_transfer` | boolean | Whether the property is for transfer. |
| `id_city` | number | City identifier. |
| `id_country` | number | Country identifier. |
| `id_property` | number | Wasi property identifier. |
| `id_property_type` | number | Property type identifier. |
| `id_region` | number | Region identifier. |
| `property_type_label` | string | Property type label. |
| `region_label` | string | Region name. |
| `rent_price` | number | Rent price. |
| `sale_price` | number | Sale price. |
| `title` | string | Property title. |

## Native endpoint

Through the native Wasi API, this operation is `GET /property/search` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

