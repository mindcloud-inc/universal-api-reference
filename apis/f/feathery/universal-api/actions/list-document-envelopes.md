# Feathery: List Document Envelopes



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-document-envelopes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-document-envelopes?connectionId=$CONNECTION_ID&id=string&type=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "type": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-document-envelopes?${params}`, {
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
| `id` | string | yes | If type is `document`, this is the document ID. If type is `user`, this is the user ID. |
| `type` | string | yes | Either `document` or `user`, specifying how to look up envelopes of interest. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "document": "string",
      "file": "string",
      "id": "string",
      "sender": "string",
      "signed": true,
      "signer": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "user": "string",
      "viewed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the envelope was created. |
| `document` | string | The document template ID when present. |
| `file` | string | The file URL for the envelope. |
| `id` | string | The envelope ID. |
| `sender` | string | The sender email when present. |
| `signed` | boolean | Whether the signer signed the envelope. |
| `signer` | string | The signer email when present. |
| `tags` | array<string> | Envelope tags. |
| `type` | string | The document type. |
| `user` | string | The Feathery user ID when present. |
| `viewed` | boolean | Whether the signer viewed the envelope. |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/document/envelope/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-envelopes.md) for the provider-specific parameters and requirements.

