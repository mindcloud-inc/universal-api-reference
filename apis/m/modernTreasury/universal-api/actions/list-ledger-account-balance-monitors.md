# Modern Treasury: List Ledger Account Balance Monitors

Retrieves ledger account balance monitors from Modern Treasury.

```
GET https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-ledger-account-balance-monitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modern Treasury `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-ledger-account-balance-monitors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-ledger-account-balance-monitors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "alertCondition": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentLedgerAccountBalanceState": {},
      "description": "string",
      "discardedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "ledgerAccountId": "string",
      "liveMode": true,
      "metadata": {},
      "object": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertCondition` | object |  |
| `createdAt` | date |  |
| `currentLedgerAccountBalanceState` | object |  |
| `description` | string |  |
| `discardedAt` | date |  |
| `id` | string |  |
| `ledgerAccountId` | string |  |
| `liveMode` | boolean |  |
| `metadata` | object |  |
| `object` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Modern Treasury API, this operation is `GET /ledger_account_balance_monitors` (base URL `https://app.moderntreasury.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ledger-account-balance-monitors.md) for the provider-specific parameters and requirements.

