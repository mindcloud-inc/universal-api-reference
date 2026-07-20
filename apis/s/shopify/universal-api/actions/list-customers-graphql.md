# Shopify: List Customers

Retrieves customers from Shopify with GraphQL.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-customers-graphql
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-customers-graphql?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-customers-graphql?${params}`, {
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
| `customerQuery` | string | no | Optional Shopify customer search query string. Leave blank to list customers. Example: `state:ENABLED`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAfter` | string | no | Optional lower bound for Shopify customer_date search, for example 2026-03-01 or 2026-03-01T00:00:00Z. Example: `2026-03-01`. |
| `createdBefore` | string | no | Optional upper bound for Shopify customer_date search, for example 2026-04-01 or 2026-04-01T00:00:00Z. Example: `2026-04-01`. |
| `updatedAfter` | string | no | Optional lower bound for Shopify updated_at search, for example 2026-03-01 or 2026-03-01T00:00:00Z. Example: `2026-03-01`. |
| `updatedBefore` | string | no | Optional upper bound for Shopify updated_at search, for example 2026-04-01 or 2026-04-01T00:00:00Z. Example: `2026-04-01`. |
| `afterCursor` | string | no | Optional cursor for manually continuing from a previous page. Standard pagination controls handle this automatically in most workflows. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountSpent": {
        "amount": "string",
        "currencyCode": "string"
      },
      "createdAt": "string",
      "defaultAddress": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "province": "string",
        "zip": "string"
      },
      "defaultEmailAddress": {
        "emailAddress": "ava@example.com"
      },
      "defaultPhoneNumber": {
        "phoneNumber": "string"
      },
      "firstName": "Ava",
      "hasNextCursor": true,
      "id": "string",
      "lastName": "Chen",
      "nextCursor": "string",
      "numberOfOrders": 1,
      "state": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "verifiedEmail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountSpent.amount` | string | Total amount the customer has spent. |
| `amountSpent.currencyCode` | string | Currency for the total amount spent. |
| `createdAt` | string | When the customer was created. |
| `defaultAddress.address1` | string | Default address line 1. |
| `defaultAddress.address2` | string | Default address line 2. |
| `defaultAddress.city` | string | Default address city. |
| `defaultAddress.country` | string | Default address country. |
| `defaultAddress.province` | string | Default address province or state. |
| `defaultAddress.zip` | string | Default address postal code. |
| `defaultEmailAddress.emailAddress` | string | Customer default email address. |
| `defaultPhoneNumber.phoneNumber` | string | Customer default phone number. |
| `firstName` | string | Customer first name. |
| `hasNextCursor` | boolean | Whether another page is available. |
| `id` | string | Shopify customer GID. |
| `lastName` | string | Customer last name. |
| `nextCursor` | string | Cursor to pass into After Cursor for next page. |
| `numberOfOrders` | number | How many orders the customer has placed. |
| `state` | string | Customer account state. |
| `tags[]` | string | Customer tags. |
| `updatedAt` | string | When the customer was last updated. |
| `verifiedEmail` | boolean | Whether the customer's email address is verified. |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers-graphql.md) for the provider-specific parameters and requirements.

