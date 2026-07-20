# Stripe: Search Customers

Finds customers in Stripe by search query.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&query=name%3A'Jane%20Doe'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "name:'Jane Doe'"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-customers?${params}`, {
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
| `query` | string | yes | Search query string, such as name:'Jane Doe' AND metadata['foo']:'bar'. Example: `name:'Jane Doe'`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Number of customers to return (1-100). Example: `100`. |
| `page` | string | no | Pagination cursor for next page from a prior search response. Example: `search_result_cursor`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "currency": "string",
      "delinquent": true,
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Creation timestamp in seconds |
| `currency` | string | Default currency |
| `delinquent` | boolean | Whether the customer is delinquent |
| `email` | string | Customer email |
| `id` | string | Customer ID |
| `name` | string | Customer name |
| `object` | string | Stripe object type |

## Native endpoint

Through the native Stripe API, this operation is `GET customers/search` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-customers.md) for the provider-specific parameters and requirements.

