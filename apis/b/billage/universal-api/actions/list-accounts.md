# Billage: List Accounts

Retrieves account records from Billage by criteria.

```
GET https://connect.mindcloud.co/v1/universal/billage/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billage/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billage/latest/actions/list-accounts?${params}`, {
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
| `q` | string | no | Search accounts |
| `type` | string | no | Filter by account type |
| `alias` | string | no | Filter by account alias |
| `name` | string | no | Filter by account name |
| `vat` | string | no | Filter by VAT number |
| `fields` | string | no | Limit returned account fields |
| `colour` | string | no | Filter by colour |
| `owner` | string | no | Filter by owner |
| `address` | string | no | Filter by address |
| `country` | string | no | Filter by country |
| `dateFrom` | string | no | Filter accounts modified after this date |
| `dateTo` | string | no | Filter accounts modified before this date |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billage API returns.

## Native endpoint

Through the native Billage API, this operation is `GET /v2/accounts` (base URL `https://app.getbillage.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

