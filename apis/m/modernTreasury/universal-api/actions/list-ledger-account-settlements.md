# Modern Treasury: List Ledger Account Settlements

Retrieves ledger account settlements from Modern Treasury.

```
GET https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-ledger-account-settlements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modern Treasury `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-ledger-account-settlements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-ledger-account-settlements?${params}`, {
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
      "contraLedgerAccountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "effectiveAtUpperBound": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "ledgerId": "string",
      "ledgerTransactionId": "string",
      "liveMode": true,
      "object": "string",
      "settledLedgerAccountId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contraLedgerAccountId` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `effectiveAtUpperBound` | date |  |
| `id` | string |  |
| `ledgerId` | string |  |
| `ledgerTransactionId` | string |  |
| `liveMode` | boolean |  |
| `object` | string |  |
| `settledLedgerAccountId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Modern Treasury API, this operation is `GET /ledger_account_settlements` (base URL `https://app.moderntreasury.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ledger-account-settlements.md) for the provider-specific parameters and requirements.

