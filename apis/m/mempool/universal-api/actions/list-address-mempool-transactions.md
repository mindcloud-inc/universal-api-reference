# Mempool: List Address Mempool Transactions

Retrieves unconfirmed transaction history for an address from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-address-mempool-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-address-mempool-transactions?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-address-mempool-transactions?${params}`, {
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
| `address` | string | yes | Bitcoin address to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fee": 1,
      "locktime": 1,
      "sigops": 1,
      "size": 1,
      "status": {},
      "txid": "string",
      "version": 1,
      "vin": [
        {}
      ],
      "vout": [
        {}
      ],
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fee` | number |  |
| `locktime` | number |  |
| `sigops` | number |  |
| `size` | number |  |
| `status` | object |  |
| `txid` | string |  |
| `version` | number |  |
| `vin` | array<object> |  |
| `vout` | array<object> |  |
| `weight` | number |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /address/[:address]/txs/mempool` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-address-mempool-transactions.md) for the provider-specific parameters and requirements.

