# CoinGate: Get Ledger Transaction

Retrieves a ledger transaction from CoinGate by ID.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-ledger-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-ledger-transaction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-ledger-transaction?${params}`, {
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
| `id` | string | yes | CoinGate ledger transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "id": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "purpose": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.id` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `purpose` | string |  |
| `type` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /ledger/transactions/:id` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ledger-transaction.md) for the provider-specific parameters and requirements.

