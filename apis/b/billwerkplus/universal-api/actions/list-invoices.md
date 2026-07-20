# Billwerkplus: List Invoices

Retrieves invoices from Billwerkplus.

```
GET https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-invoices?${params}`, {
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
| `range` | list | no | Time attribute to limit by: created or settled. One of: `0`, `1`. Default: `created`. |
| `handle` | string | no | Exact invoice handle. |
| `handlePrefix` | string | no | Invoice handle prefix. |
| `handleContains` | string | no | Invoice handle contains filter. |
| `state[]` | array<string> | no | Invoice states to include. Multiple values are allowed. Accepts multiple values as an array. |
| `customer` | string | no | Customer handle filter. |
| `currency[]` | array<string> | no | Invoice currency filter. Multiple values are allowed. Accepts multiple values as an array. |
| `type[]` | array<string> | no | Invoice types to include. Multiple values are allowed. Accepts multiple values as an array. |
| `subscription` | string | no | Subscription handle filter. |
| `plan` | string | no | Subscription plan handle filter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | date | no | Inclusive start of the local account time range. |
| `to` | date | no | Exclusive end of the local account time range. |
| `interval` | string | no | ISO 8601 duration counted back from To. |
| `due` | date | no | Due date filter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billwerkplus API returns.

## Native endpoint

Through the native Billwerkplus API, this operation is `GET /list/invoice` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

