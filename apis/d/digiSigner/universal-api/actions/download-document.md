# DigiSigner: Download Document

Downloads a document from DigiSigner by ID.

```
GET https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/download-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiSigner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/download-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/download-document?${params}`, {
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
| `documentId` | string | yes | DigiSigner document_id returned by Upload Document or a template ID where the endpoint accepts one. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native DigiSigner API, this operation is `GET /documents/:documentId` (base URL `https://api.digisigner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-document.md) for the provider-specific parameters and requirements.

