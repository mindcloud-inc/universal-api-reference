# Jobber: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobber `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-invoices?${params}`, {
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
| `columns` | string | no | Select the Jobber invoice fields to return. Default: `["id","invoiceNumber","invoiceStatus","subject","message","createdAt","updatedAt","dueDate","issuedDate","receivedDate","jobberWebUri","client.id","client.name","client.firstName","client.lastName","jobs.nodes.id","jobs.nodes.jobNumber","properties.nodes.id"]`. |
| `createdAfter` | date | no | Only return invoices created after this timestamp (ISO 8601). Maps to filter.createdAt.after on the Jobber invoices query. Example: `2026-04-01T00:00:00.000Z`. |
| `createdBefore` | date | no | Only return invoices created before this timestamp (ISO 8601). Maps to filter.createdAt.before on the Jobber invoices query. |
| `clientId` | string | no | Only return invoices for the specified Jobber client id. |
| `invoiceNumber` | string | no | Only return the invoice matching the specified invoice number. |
| `status` | string | no | Only return invoices with the specified Jobber invoice status. |
| `excludeOrigin` | string | no | Exclude invoices with one or more of the specified Jobber invoice origins. Accepts multiple values as an array. |
| `updatedAfter` | date | no | Only return invoices updated after this timestamp (ISO 8601). Maps to filter.updatedAt.after on the Jobber invoices query. Example: `2026-04-01T00:00:00.000Z`. |
| `updatedBefore` | date | no | Only return invoices updated before this timestamp (ISO 8601). Maps to filter.updatedAt.before on the Jobber invoices query. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jobber API returns.

## Native endpoint

Through the native Jobber API, this operation is `POST graphql` (base URL `https://api.getjobber.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

