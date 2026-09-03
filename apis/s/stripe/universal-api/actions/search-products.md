# Stripe: Search Products



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-products?connectionId=$CONNECTION_ID&query=active%3A'true'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "active:'true'"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-products?${params}`, {
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
| `query` | string | yes | Example: `active:'true'`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": 1,
      "defaultPrice": "string",
      "description": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | number |  |
| `defaultPrice` | string |  |
| `description` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `updated` | number |  |

## Native endpoint

Through the native Stripe API, this operation is `GET products/search` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

