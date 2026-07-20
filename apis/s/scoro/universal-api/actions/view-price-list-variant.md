# Scoro: View Price List Variant

Retrieves price list variant details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-price-list-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-price-list-variant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-price-list-variant?${params}`, {
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
| `id` | string | no | Scoro local price list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_date": "string",
      "currency": "string",
      "id": 1,
      "modified_date": "string",
      "name": "Ava Chen",
      "price_list_id": 1,
      "role_prices": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_date` | string |  |
| `currency` | string |  |
| `id` | number |  |
| `modified_date` | string |  |
| `name` | string |  |
| `price_list_id` | number |  |
| `role_prices` | array<object> |  |

## Native endpoint

Through the native Scoro API, this operation is `POST localPriceLists/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-price-list-variant.md) for the provider-specific parameters and requirements.

