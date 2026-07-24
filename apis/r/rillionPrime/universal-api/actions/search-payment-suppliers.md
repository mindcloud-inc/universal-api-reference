# Rillion Prime Pay: Search Payment Suppliers



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/search-payment-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/search-payment-suppliers?connectionId=$CONNECTION_ID&search=Acme" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "Acme"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/search-payment-suppliers?${params}`, {
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
| `search` | string | yes | Search term used to find suppliers. Example: `Acme`. |
| `limit` | number | no | Maximum number of supplier results to return. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "supplier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `supplier` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/supplier/typeahead` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-payment-suppliers.md) for the provider-specific parameters and requirements.

