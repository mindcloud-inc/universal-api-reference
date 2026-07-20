# Wasi: List Cities With Property

Retrieves cities with assigned properties from Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-cities-with-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-cities-with-property?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-cities-with-property?${params}`, {
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
| `for_rent` | boolean | no | Only include rental inventory. |
| `for_sale` | boolean | no | Only include sale inventory. |
| `for_transfer` | boolean | no | Only include transfer inventory. |
| `property_type_id` | number | no | Limit cities to one property type. |
| `scope` | number | no | Choose which Wasi inventory scope to inspect. |
| `with_country` | boolean | no | Include country information when available. |
| `with_region` | boolean | no | Include region information when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_label": "string",
      "id_city": 1,
      "id_country": 1,
      "id_region": 1,
      "name": "Ava Chen",
      "region_label": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_label` | string | Country name when with_country=true. |
| `id_city` | number | Wasi city identifier. |
| `id_country` | number | Country identifier when with_country=true. |
| `id_region` | number | Region identifier when with_region=true. |
| `name` | string | City name. |
| `region_label` | string | Region name when with_region=true. |
| `total` | number | Property count for the city. |

## Native endpoint

Through the native Wasi API, this operation is `GET /location/cities-with-property` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cities-with-property.md) for the provider-specific parameters and requirements.

