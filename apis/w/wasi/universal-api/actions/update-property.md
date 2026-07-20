# Wasi: Update Property

Updates an existing property in Wasi.

```
PUT https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "property_id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "property_id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Property address. |
| `area` | number | no | Property area. |
| `bathrooms` | number | no | Bathroom count. |
| `bedrooms` | number | no | Bedroom count. |
| `built_area` | number | no | Built area. |
| `city_id` | number | no | City ID. |
| `country_id` | number | no | Country ID. |
| `for_rent` | boolean | no | Whether the property is for rent. |
| `for_sale` | boolean | no | Whether the property is for sale. |
| `for_transfer` | boolean | no | Whether the property is for transfer. |
| `garages` | number | no | Garage count. |
| `location_id` | number | no | Locality ID. |
| `observations` | string | no | Property observations. |
| `property_id` | number | yes | Wasi property ID to update. Default: `1`. |
| `property_type_id` | number | no | Property type ID. |
| `region_id` | number | no | Region ID. |
| `rent_price` | number | no | Property rent price. |
| `sale_price` | number | no | Property sale price. |
| `title` | string | no | Property title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Wasi operation status. |

## Native endpoint

Through the native Wasi API, this operation is `POST /property/update/:id_property` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property.md) for the provider-specific parameters and requirements.

