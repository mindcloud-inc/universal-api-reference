# Customer.io: Search Customers

Finds customers in Customer.io by filter.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/search-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/search-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&filter=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "filter": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/search-customers?${params}`, {
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
| `filter` | object | yes | A Customer.io audience filter object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cioId": "string",
      "email": "ava@example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cioId` | string | The Customer.io person identifier. |
| `email` | string | The customer email address. |
| `id` | string | The customer identifier. |

## Native endpoint

Through the native Customer.io API, this operation is `POST /v1/customers` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-customers.md) for the provider-specific parameters and requirements.

