# Lunch Money: Get all accounts synced via Plaid



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-plaid-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-plaid-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-plaid-accounts?${params}`, {
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
      "allowTransactionModifications": true,
      "balance": "string",
      "balanceLastUpdate": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dateLinked": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "id": 1,
      "importStartDate": "2026-05-07T12:00:00.000Z",
      "institutionName": "Ava Chen",
      "lastFetch": "2026-05-07T12:00:00.000Z",
      "lastImport": "2026-05-07T12:00:00.000Z",
      "limit": 1,
      "linkedByName": "https://example.com",
      "mask": "string",
      "name": "Ava Chen",
      "plaidItemId": "string",
      "plaidLastSuccessfulUpdate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subtype": "string",
      "toBase": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowTransactionModifications` | boolean |  |
| `balance` | string |  |
| `balanceLastUpdate` | date |  |
| `currency` | string |  |
| `dateLinked` | date |  |
| `displayName` | string |  |
| `id` | number |  |
| `importStartDate` | date |  |
| `institutionName` | string |  |
| `lastFetch` | date |  |
| `lastImport` | date |  |
| `limit` | number |  |
| `linkedByName` | string |  |
| `mask` | string |  |
| `name` | string |  |
| `plaidItemId` | string |  |
| `plaidLastSuccessfulUpdate` | date |  |
| `status` | string |  |
| `subtype` | string |  |
| `toBase` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /plaid_accounts` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-plaid-accounts.md) for the provider-specific parameters and requirements.

