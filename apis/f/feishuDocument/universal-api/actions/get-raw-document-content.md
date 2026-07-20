# Feishu Document: Get Raw Document Content

Retrieves raw text content from a Feishu document.

```
GET https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-raw-document-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Document `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-raw-document-content?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-raw-document-content?${params}`, {
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
| `documentId` | string | yes | The unique document token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "content": "string"
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Provider error code. Zero means success. |
| `data.content` | string | Plain-text document content. |
| `msg` | string | Provider status message. |

## Native endpoint

Through the native Feishu Document API, this operation is `GET /open-apis/docx/v1/documents/:document_id/raw_content` (base URL `https://open.larksuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-raw-document-content.md) for the provider-specific parameters and requirements.

