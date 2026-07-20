# Escrow.com: List Partner Customers

Retrieves partner customers from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-partner-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-partner-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-partner-customers?${params}`, {
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
| `limit` | number | no | Maximum partner customers to fetch. |
| `nextCursor` | number | no | Cursor to start fetching partner customers from. |
| `sortBy` | string | no | Partner customer sort field. Escrow.com documents id as a valid value. |
| `sortDirection` | string | no | Sort direction, asc or desc. |
| `country` | string | no | Filter customers by country code, such as AU or US. |
| `verificationStatus` | string | no | Filter customers by verification status: verified, not_verified, or company_verified. |
| `ids[]` | array<number> | no | Customer IDs to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "disbursementMethods": [
        {}
      ],
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "verification": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Customer address details. |
| `disbursementMethods` | array<object> | Customer disbursement methods when returned. |
| `displayName` | string | Customer display name when provided. |
| `email` | string | Customer email address. |
| `firstName` | string | Customer first name. |
| `id` | number | Escrow.com customer ID. |
| `lastName` | string | Customer last name. |
| `verification` | object | Customer verification details. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /partner/customers` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-partner-customers.md) for the provider-specific parameters and requirements.

