# CommercioNetwork: Get Receipt Process

Retrieves a receipt process from CommercioNetwork.

```
GET https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-receipt-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-receipt-process?connectionId=$CONNECTION_ID&processId=bbdcc90a-..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processId": "bbdcc90a-..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-receipt-process?${params}`, {
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
| `processId` | string | yes | The receipt process ID. Example: `bbdcc90a-...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chain_id": "string",
      "created_at": "string",
      "document_tx_hash": "string",
      "document_uuid": "string",
      "error": "string",
      "process_id": "string",
      "proof": "string",
      "recipient": "string",
      "sender": "string",
      "status": "string",
      "tx_hash": "string",
      "tx_timestamp": "string",
      "tx_type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chain_id` | string | The blockchain network identifier. |
| `created_at` | string | The enqueue timestamp. |
| `document_tx_hash` | string | The document transaction hash. |
| `document_uuid` | string | The shared-document UUID. |
| `error` | string | The process failure reason when present. |
| `process_id` | string | The receipt process identifier. |
| `proof` | string | The optional reading proof. |
| `recipient` | string | The recipient DID. |
| `sender` | string | The sender DID. |
| `status` | string | The process status. |
| `tx_hash` | string | The blockchain transaction hash. |
| `tx_timestamp` | string | The blockchain timestamp. |
| `tx_type` | string | The blockchain message type. |
| `uuid` | string | The receipt UUID. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `GET /receipts/process/:process_id` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-receipt-process.md) for the provider-specific parameters and requirements.

