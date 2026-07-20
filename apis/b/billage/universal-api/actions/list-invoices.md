# Billage: List Invoices

Retrieves invoice records from Billage by code or date.

```
GET https://connect.mindcloud.co/v1/universal/billage/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billage/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billage/latest/actions/list-invoices?${params}`, {
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
| `q` | string | no | Search invoices |
| `account` | string | no | Account |
| `colour` | string | no | Colour name |
| `dateFrom` | date | no | Date from (yyyy-MM-dd) |
| `dateTo` | date | no | Date to (yyyy-MM-dd) |
| `ref` | string | no | Reference code |
| `serie` | string | no | Serie |
| `owner` | string | no | Invoice owner |
| `state` | string | no | Invoice state |
| `category` | string | no | Invoice category |
| `tags[]` | array<string> | no | Invoice tags |
| `summarized` | boolean | no | Summarized |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billage API returns.

## Native endpoint

Through the native Billage API, this operation is `GET /v2/invoices` (base URL `https://app.getbillage.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

