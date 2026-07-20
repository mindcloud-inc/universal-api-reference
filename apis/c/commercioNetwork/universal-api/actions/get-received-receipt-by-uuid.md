# CommercioNetwork: Get Received Receipt by UUID

Retrieves a received receipt from CommercioNetwork by UUID.

```
GET https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-received-receipt-by-uuid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-received-receipt-by-uuid?connectionId=$CONNECTION_ID&receiptUuid=f6b6a60e-..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "receiptUuid": "f6b6a60e-..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-received-receipt-by-uuid?${params}`, {
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
| `receiptUuid` | string | yes | The received receipt UUID. Example: `f6b6a60e-...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_tx_hash": "string",
      "document_uuid": "string",
      "proof": "string",
      "recipient": "string",
      "sender": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_tx_hash` | string | The document transaction hash. |
| `document_uuid` | string | The shared-document UUID. |
| `proof` | string | The optional reading proof. |
| `recipient` | string | The recipient DID. |
| `sender` | string | The sender DID. |
| `uuid` | string | The receipt UUID. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `GET /receipts/received/:uuid` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-received-receipt-by-uuid.md) for the provider-specific parameters and requirements.

