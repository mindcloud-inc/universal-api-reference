# Bridge: List Transactions

Retrieves transactions from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-transactions?connectionId=$CONNECTION_ID&userAccessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userAccessToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-transactions?${params}`, {
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
| `userAccessToken` | string | yes | Bridge user access token returned by the Authorization token action. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | no | Filter transactions by account |
| `since` | date | no | Limit transactions to those with an `updated_at` value after the specified timestamp |
| `until` | date | no | Limit transactions to those with an `updated_at` value before the specified timestamp |
| `minDate` | date | no | Limit transactions to those with a `date` value after the specified date |
| `maxDate` | date | no | Limit transactions to those with a `date` value before the specified date |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridge API returns.

## Native endpoint

Through the native Bridge API, this operation is `GET /aggregation/transactions` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

