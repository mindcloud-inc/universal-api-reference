# Yousign: Download Signature Request Documents

Downloads documents from a Yousign signature request.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/download-signature-request-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/download-signature-request-documents?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/download-signature-request-documents?${params}`, {
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
| `signatureRequestId` | string | yes | The Yousign signature request ID. |
| `version` | string | no | Which document version to download. |
| `archive` | boolean | no | Force ZIP archive download. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yousign API returns.

## Native endpoint

Through the native Yousign API, this operation is `GET /signature_requests/:signatureRequestId/documents/download` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-signature-request-documents.md) for the provider-specific parameters and requirements.

