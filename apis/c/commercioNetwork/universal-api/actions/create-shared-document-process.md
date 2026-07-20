# CommercioNetwork: Create Shared Document Process

Creates a shared document process in CommercioNetwork.

```
POST https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/create-shared-document-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/create-shared-document-process" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentUri": "https://mindcloud.invalid/commercio/document.txt",
  "hash": "79b9ff20...",
  "hashAlgorithm": "sha-256",
  "recipients[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/create-shared-document-process', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentUri": "https://mindcloud.invalid/commercio/document.txt",
    "hash": "79b9ff20...",
    "hashAlgorithm": "sha-256",
    "recipients[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentUri` | string | yes | The document URI recorded in Commercio. Example: `https://mindcloud.invalid/commercio/document.txt`. |
| `hash` | string | yes | The SHA-256 hash of the document content. Example: `79b9ff20...`. |
| `hashAlgorithm` | string | yes | The hashing algorithm used for the document hash. Default: `sha-256`. Example: `sha-256`. |
| `recipients[]` | array<string> | yes | One or more recipient wallet addresses in DID format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "doc_hash": "string",
      "doc_hash_alg": "string",
      "doc_metadata": {},
      "doc_storage_uri": "string",
      "document_id": "string",
      "process_id": "string",
      "receivers": [
        "string"
      ],
      "sender": "string",
      "status": "string",
      "timestamp": "string",
      "tx_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `doc_hash` | string | The document checksum hash. |
| `doc_hash_alg` | string | The hash algorithm. |
| `doc_metadata` | object | The document metadata payload. |
| `doc_storage_uri` | string | The document storage URI. |
| `document_id` | string | The created shared-document UUID. |
| `process_id` | string | The queued shared-document process identifier. |
| `receivers` | array<string> | The recipient DID list. |
| `sender` | string | The sender DID. |
| `status` | string | The process status. |
| `timestamp` | string | The enqueue timestamp. |
| `tx_type` | string | The blockchain message type. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `POST /sharedoc/process` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shared-document-process.md) for the provider-specific parameters and requirements.

