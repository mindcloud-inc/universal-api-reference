# Stripe: List Customers

Retrieves customers from your Stripe account.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customers?${params}`, {
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
| `email` | string | no | Case-sensitive customer email filter. Example: `customer@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `created` | object | no | Date interval object for customer creation timestamp filters. |
| `created.gt` | number | no | Minimum creation timestamp (exclusive). Example: `1704067200`. |
| `created.gte` | number | no | Minimum creation timestamp (inclusive). Example: `1704067200`. |
| `created.lt` | number | no | Maximum creation timestamp (exclusive). Example: `1706745600`. |
| `created.lte` | number | no | Maximum creation timestamp (inclusive). Example: `1706745600`. |
| `limit` | number | no | Number of customers to return (1-100). Example: `100`. |
| `startingAfter` | string | no | Pagination cursor for next page. Example: `cus_123`. |
| `endingBefore` | string | no | Pagination cursor for previous page. Example: `cus_123`. |
| `testClock` | string | no | Filter to customers attached to a test clock. Example: `clock_123`. |

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

Through the native Stripe API, this operation is `GET customers` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

