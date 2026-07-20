# Customer.io: List Customers by Email

Finds customers in Customer.io by email address.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-by-email?connectionId=$CONNECTION_ID&email=jane%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "jane@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-by-email?${params}`, {
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
| `email` | string | yes | The email address to search for. Example: `jane@example.com`. |

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

Through the native Customer.io API, this operation is `GET /v1/customers` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers-by-email.md) for the provider-specific parameters and requirements.

