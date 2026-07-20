# Mercado Pago: Search Preferences

Finds checkout preferences in Mercado Pago by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-preferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-preferences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/search-preferences?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sponsor_id` | number | no |  |
| `external_reference` | string | no |  |
| `site_id` | string | no |  |
| `marketplace` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elements": [
        [
          {}
        ]
      ],
      "next_offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements[]` | array<object> |  |
| `next_offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Mercado Pago API, this operation is `GET /checkout/preferences/search` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-preferences.md) for the provider-specific parameters and requirements.

