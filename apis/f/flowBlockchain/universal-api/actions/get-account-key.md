# Flow Blockchain: Get Account Key

Retrieves an account key from Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-account-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-account-key?connectionId=$CONNECTION_ID&address=string&index=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string",
  "index": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-account-key?${params}`, {
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
| `address` | string | yes | Flow account address. |
| `index` | string | yes | Index of the Flow account key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hashing_algorithm": "string",
      "index": "string",
      "public_key": "string",
      "revoked": true,
      "sequence_number": "string",
      "signing_algorithm": "string",
      "weight": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hashing_algorithm` | string | Hashing algorithm. |
| `index` | string | Account key index. |
| `public_key` | string | Public key. |
| `revoked` | boolean | Whether the key is revoked. |
| `sequence_number` | string | Key sequence number. |
| `signing_algorithm` | string | Signing algorithm. |
| `weight` | string | Key weight. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /accounts/{address}/keys/{index}` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-key.md) for the provider-specific parameters and requirements.

