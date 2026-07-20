# Fiserv: Search Transactions

Finds transactions in Fiserv by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/search-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/search-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/search-transactions?${params}`, {
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
| `rootSourceId` | string | no | Root source ID such as payment, refund, or dispute ID. |
| `sourceType` | list | no | Transaction source type filter. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `settlementStatus` | list | no | Settlement status filter. One of: `0`, `1`. |
| `createdAtStart` | date | no | Start of created_at date-time range. |
| `createdAtEnd` | date | no | End of created_at date-time range. |
| `sortColumn` | list | no | Sort column. One of: `0`, `1`, `2`, `3`, `4`. |
| `sortDirection` | list | no | Sort direction. One of: `0`, `1`. |
| `amountMin` | number | no | Minimum transaction amount. |
| `amountMax` | number | no | Maximum transaction amount. |
| `limit` | number | no | Maximum number of rows. Official max is 50. |
| `page` | number | no | Page number, starting at 1. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `POST /transactions/search` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-transactions.md) for the provider-specific parameters and requirements.

