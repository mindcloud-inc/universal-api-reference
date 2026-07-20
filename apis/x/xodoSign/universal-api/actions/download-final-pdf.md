# Xodo Sign: Download Final PDF

Retrieves the final PDF from Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/download-final-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/download-final-pdf?connectionId=$CONNECTION_ID&business_id=string&document_hash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_id": "string",
  "document_hash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/download-final-pdf?${params}`, {
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
| `business_id` | string | yes | The Xodo Sign business ID that owns the document. |
| `document_hash` | string | yes | The unique document hash to download. |
| `audit_trail` | string | no | Set to 1 to attach the audit trail to the final PDF. |
| `document_id` | string | no | Optional file selector for multi-file documents or AT for audit trail only. |
| `url_only` | string | no | Set to 1 to return only the download URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdf_binary_or_download_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdf_binary_or_download_url` | string | Binary PDF content by default, or a download URL when `url_only=1` is used. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /download_final_document` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-final-pdf.md) for the provider-specific parameters and requirements.

