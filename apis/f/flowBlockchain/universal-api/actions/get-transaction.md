# Flow Blockchain: Get Transaction

Retrieves a transaction from Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-transaction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-transaction?${params}`, {
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
| `id` | string | yes | Transaction ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arguments": [
        "string"
      ],
      "authorizers": [
        "string"
      ],
      "envelope_signatures": [
        {}
      ],
      "gas_limit": "string",
      "id": "string",
      "payer": "string",
      "payload_signatures": [
        {}
      ],
      "proposal_key": {},
      "reference_block_id": "string",
      "script": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arguments` | array<string> | Cadence transaction arguments. |
| `authorizers` | array<string> | Authorizer addresses. |
| `envelope_signatures` | array<object> | Envelope signatures. |
| `gas_limit` | string | Gas limit. |
| `id` | string | Flow transaction ID. |
| `payer` | string | Payer address. |
| `payload_signatures` | array<object> | Payload signatures. |
| `proposal_key` | object | Proposal key. |
| `reference_block_id` | string | Reference block ID. |
| `script` | string | Base64-encoded Cadence script. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /transactions/{id}` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

