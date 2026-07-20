# CommercioNetwork: Create Receipt

Creates a receipt process in CommercioNetwork.

```
POST https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/create-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/create-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentTxHash": "CDE319A5...",
  "documentUuid": "41a2b679-..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/create-receipt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentTxHash": "CDE319A5...",
    "documentUuid": "41a2b679-..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentTxHash` | string | yes | The transaction hash of the shared document. Example: `CDE319A5...`. |
| `documentUuid` | string | yes | The UUID of the shared document. Example: `41a2b679-...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "document_tx_hash": "string",
      "document_uuid": "string",
      "process_id": "string",
      "recipient": "string",
      "sender": "string",
      "status": "string",
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
| `created_at` | string | The enqueue timestamp. |
| `document_tx_hash` | string | The document transaction hash. |
| `document_uuid` | string | The shared-document UUID. |
| `process_id` | string | The queued receipt process identifier. |
| `recipient` | string | The recipient DID. |
| `sender` | string | The sender DID. |
| `status` | string | The process status. |
| `tx_type` | string | The blockchain message type. |
| `uuid` | string | The receipt UUID. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `POST /receipts` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-receipt.md) for the provider-specific parameters and requirements.

