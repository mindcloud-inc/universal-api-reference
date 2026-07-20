# Fintoc: Create Transfer

Creates a transfer in Fintoc.

```
POST https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fintocJwsSignature": "<paste jws signature>",
  "amount": "1000",
  "currency": "MXN",
  "accountId": "acc_...",
  "counterparty": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fintocJwsSignature": "<paste jws signature>",
    "amount": "1000",
    "currency": "MXN",
    "accountId": "acc_...",
    "counterparty": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Transfer amount in minor units. Example: `1000`. |
| `currency` | string | yes | Transfer currency. Example: `MXN`. |
| `accountId` | string | yes | Source account ID for the transfer. Example: `acc_...`. |
| `counterparty` | object | yes | Destination counterparty object. For MXN use at least `{ "account_number": "..." }`. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fintocJwsSignature` | string | yes | Per-request JWS signature for transfer creation. Example: `<paste jws signature>`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_number": {},
      "amount": 1,
      "comment": "string",
      "counterparty": {},
      "currency": "string",
      "direction": "string",
      "id": "string",
      "metadata": {},
      "mode": "string",
      "object": "string",
      "post_date": "string",
      "receipt_url": "https://example.com",
      "reference_id": "string",
      "return_reason": "string",
      "status": "string",
      "tracking_key": "string",
      "transaction_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_number` | object |  |
| `amount` | number |  |
| `comment` | string |  |
| `counterparty` | object |  |
| `currency` | string |  |
| `direction` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `mode` | string |  |
| `object` | string |  |
| `post_date` | string |  |
| `receipt_url` | string |  |
| `reference_id` | string |  |
| `return_reason` | string |  |
| `status` | string |  |
| `tracking_key` | string |  |
| `transaction_date` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `POST /v2/transfers` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transfer.md) for the provider-specific parameters and requirements.

