# CommercioNetwork: Get Shared Document Process

Retrieves a shared document process from CommercioNetwork.

```
GET https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-shared-document-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-shared-document-process?connectionId=$CONNECTION_ID&processId=510c305a-..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processId": "510c305a-..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-shared-document-process?${params}`, {
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
| `processId` | string | yes | The shared document process ID. Example: `510c305a-...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chain_id": "string",
      "doc_hash": "string",
      "doc_hash_alg": "string",
      "doc_metadata": {},
      "doc_storage_uri": "string",
      "doc_tx_hash": "string",
      "document_id": "string",
      "process_id": "string",
      "receivers": [
        "string"
      ],
      "sender": "string",
      "status": "string",
      "timestamp": "string",
      "tx_timestamp": "string",
      "tx_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chain_id` | string | The blockchain network identifier. |
| `doc_hash` | string | The document checksum hash. |
| `doc_hash_alg` | string | The hash algorithm. |
| `doc_metadata` | object | The document metadata payload. |
| `doc_storage_uri` | string | The document storage URI. |
| `doc_tx_hash` | string | The blockchain transaction hash. |
| `document_id` | string | The shared-document UUID. |
| `process_id` | string | The shared-document process identifier. |
| `receivers` | array<string> | The recipient DID list. |
| `sender` | string | The sender DID. |
| `status` | string | The process status. |
| `timestamp` | string | The enqueue timestamp. |
| `tx_timestamp` | string | The blockchain timestamp. |
| `tx_type` | string | The blockchain message type. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `GET /sharedoc/process/:process_id` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shared-document-process.md) for the provider-specific parameters and requirements.

