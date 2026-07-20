# Flow Blockchain: Execute Cadence Script

Executes a Cadence script on Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/execute-cadence-script
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/execute-cadence-script?connectionId=$CONNECTION_ID&script=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "script": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/execute-cadence-script?${params}`, {
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
| `arguments[]` | array<string> | no | Cadence arguments encoded as Base64 JSON-Cadence values. |
| `blockHeight` | string | no | Optional block height to execute the script against. Incompatible with block ID. |
| `blockId` | string | no | Optional block ID to execute the script against. |
| `script` | string | yes | Base64-encoded Cadence script to execute. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `type` | string | Cadence value type. |
| `value` | string | Cadence value payload. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `POST /scripts` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-cadence-script.md) for the provider-specific parameters and requirements.

