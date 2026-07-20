# DigiSigner: Get Document Fields

Retrieves document fields from DigiSigner by document ID.

```
GET https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-document-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiSigner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-document-fields?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-document-fields?${params}`, {
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
| `documentId` | string | yes | DigiSigner document_id whose fields should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_fields": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_fields` | array<object> | Fields on the document, including signer-submitted content. |

## Native endpoint

Through the native DigiSigner API, this operation is `GET /documents/:documentId/fields` (base URL `https://api.digisigner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-fields.md) for the provider-specific parameters and requirements.

