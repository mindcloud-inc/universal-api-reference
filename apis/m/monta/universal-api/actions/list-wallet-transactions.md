# Monta: List Wallet Transactions

Retrieves wallet transactions from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-wallet-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-wallet-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/list-wallet-transactions?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `state` | list<string> | no | Only return wallet transactions in this state. One of: `complete`, `failed`, `pending`, `reserved`. Default: `complete`. |
| `fromDate` | date | no | Only return wallet transactions created at or after this ISO 8601 date-time. Example: `2022-05-22T09:30:03Z`. |
| `toDate` | date | no | Only return wallet transactions created at or before this ISO 8601 date-time. Example: `2022-05-22T09:30:03Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "exchangeRate": 1,
      "fromAmount": 1,
      "fromCurrency": {
        "decimals": 1,
        "identifier": "string",
        "name": "Ava Chen"
      },
      "fromWalletId": 1,
      "id": 1,
      "note": "string",
      "state": "string",
      "summary": "string",
      "toAmount": 1,
      "toCurrency": {
        "decimals": 1,
        "identifier": "string",
        "name": "Ava Chen"
      },
      "toWalletId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `exchangeRate` | number |  |
| `fromAmount` | number |  |
| `fromCurrency.decimals` | number |  |
| `fromCurrency.identifier` | string |  |
| `fromCurrency.name` | string |  |
| `fromWalletId` | number |  |
| `id` | number |  |
| `note` | string |  |
| `state` | string |  |
| `summary` | string |  |
| `toAmount` | number |  |
| `toCurrency.decimals` | number |  |
| `toCurrency.identifier` | string |  |
| `toCurrency.name` | string |  |
| `toWalletId` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Monta API, this operation is `GET /wallet-transactions` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-wallet-transactions.md) for the provider-specific parameters and requirements.

