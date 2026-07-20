# Wasi: List Countries

Retrieves countries from Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-countries?${params}`, {
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
| `for_rent` | boolean | no | Only count properties available for rent. |
| `for_sale` | boolean | no | Only count properties available for sale. |
| `for_transfer` | boolean | no | Only count properties available for transfer. |
| `property_type_id` | number | no | Limit quantity counts to one property type. |
| `quantity` | boolean | no | Include the number of matching properties per country. |
| `scope` | number | no | Choose which property scope to count. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id_country": 1,
      "iso": "string",
      "name": "Ava Chen",
      "quantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id_country` | number | Wasi country identifier. |
| `iso` | string | ISO country code. |
| `name` | string | Country name. |
| `quantity` | number | Property count when quantity=true is requested. |

## Native endpoint

Through the native Wasi API, this operation is `GET /location/all-countries` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries.md) for the provider-specific parameters and requirements.

