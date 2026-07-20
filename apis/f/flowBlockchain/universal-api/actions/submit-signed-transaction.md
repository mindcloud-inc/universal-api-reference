# Flow Blockchain: Submit Signed Transaction

Submits a signed transaction to Flow Blockchain.

```
POST https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/submit-signed-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/submit-signed-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "arguments[]": [
    "string"
  ],
  "authorizers[]": [
    "string"
  ],
  "envelopeSignatures[]": [
    {}
  ],
  "gasLimit": "string",
  "payer": "string",
  "payloadSignatures[]": [
    {}
  ],
  "proposalKey": {},
  "referenceBlockId": "string",
  "script": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/submit-signed-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "arguments[]": ["string"],
    "authorizers[]": ["string"],
    "envelopeSignatures[]": [{}],
    "gasLimit": "string",
    "payer": "string",
    "payloadSignatures[]": [{}],
    "proposalKey": {},
    "referenceBlockId": "string",
    "script": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `arguments[]` | array<string> | yes | Array of Base64-encoded JSON-Cadence transaction arguments. |
| `authorizers[]` | array<string> | yes | Flow addresses authorizing the transaction. |
| `envelopeSignatures[]` | array<object> | yes | Envelope signature objects for the already-signed transaction. |
| `gasLimit` | string | yes | Maximum computation units allowed for the transaction. |
| `payer` | string | yes | Flow address paying transaction fees. |
| `payloadSignatures[]` | array<object> | yes | Payload signature objects for the already-signed transaction. |
| `proposalKey` | object | yes | Proposal key object with address, key index, and sequence number. |
| `referenceBlockId` | string | yes | Reference block ID for the signed transaction. |
| `script` | string | yes | Base64-encoded Cadence transaction script. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Flow API resource links. |
| `id` | string | Submitted Flow transaction ID. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `POST /transactions` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-signed-transaction.md) for the provider-specific parameters and requirements.

