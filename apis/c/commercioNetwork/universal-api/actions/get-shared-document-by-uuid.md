# CommercioNetwork: Get Shared Document by UUID

Retrieves a shared document from CommercioNetwork by UUID.

```
GET https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-shared-document-by-uuid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-shared-document-by-uuid?connectionId=$CONNECTION_ID&documentUuid=41a2b679-..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentUuid": "41a2b679-..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-shared-document-by-uuid?${params}`, {
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
| `documentUuid` | string | yes | The shared document UUID. Example: `41a2b679-...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checksum": {},
      "content_uri": "string",
      "do_sign": {},
      "encryption_data": {},
      "metadata": {},
      "recipients": [
        "string"
      ],
      "sender": "string",
      "tx_hash": "string",
      "tx_timestamp": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checksum` | object | The optional document checksum. |
| `content_uri` | string | The document content URI. |
| `do_sign` | object | The signing metadata for the document. |
| `encryption_data` | object | The optional encryption metadata. |
| `metadata` | object | The document metadata payload. |
| `recipients` | array<string> | The recipient DID list. |
| `sender` | string | The sender DID. |
| `tx_hash` | string | The blockchain transaction hash. |
| `tx_timestamp` | string | The blockchain timestamp. |
| `uuid` | string | The shared-document UUID. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `GET /sharedoc/:document_uuid` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shared-document-by-uuid.md) for the provider-specific parameters and requirements.

