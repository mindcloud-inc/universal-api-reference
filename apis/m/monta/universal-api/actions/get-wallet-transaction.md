# Monta: Get Wallet Transaction

Retrieves a wallet transaction from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-wallet-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-wallet-transaction?connectionId=$CONNECTION_ID&transactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-wallet-transaction?${params}`, {
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
| `transactionId` | number | yes | ID of the wallet transaction to retrieve. |

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

Through the native Monta API, this operation is `GET /wallet-transactions/{transactionId}` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-transaction.md) for the provider-specific parameters and requirements.

