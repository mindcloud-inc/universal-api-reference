# Checkout Page: List Customers

Retrieves customers from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-customers?${params}`, {
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
| `limit` | string | no | The number of results per page. Minimum value is 1 and maximum is 100. Defaults to 20. |
| `startingAfter` | string | no | A cursor value specifying the id of a resource to start before. Retrieves items that appear after this cursor in the list. Cannot be used together with `ending_before`. |
| `endingBefore` | string | no | A cursor value specifying the id of a resource to end after. Retrieves items that appear before this cursor in the list. Cannot be used together with `starting_after`. |
| `search` | string | no | List all customers |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "billingEmail": "ava@example.com",
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "sellerId": "string",
      "shipping": {},
      "stripeCustomerId": "string",
      "taxId": "string",
      "taxIdType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `billingEmail` | string |  |
| `companyName` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `sellerId` | string |  |
| `shipping` | object |  |
| `stripeCustomerId` | string |  |
| `taxId` | string |  |
| `taxIdType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/customers/` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

