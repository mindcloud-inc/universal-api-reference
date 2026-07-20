# Feishu Document: Get Document

Retrieves document details from Feishu Docs.

```
GET https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Document `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-document?${params}`, {
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
        "document": {
          "display_setting": {
            "show_authors": true,
            "show_comment_count": true
          },
          "document_id": "string",
          "revision_id": 1,
          "title": "string"
        }
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
| `data.document.display_setting.show_authors` | boolean | Whether author display is enabled. |
| `data.document.display_setting.show_comment_count` | boolean | Whether comment count display is enabled. |
| `data.document.document_id` | string | Document token. |
| `data.document.revision_id` | number | Current document revision id. |
| `data.document.title` | string | Document title. |
| `msg` | string | Provider status message. |

## Native endpoint

Through the native Feishu Document API, this operation is `GET /open-apis/docx/v1/documents/:document_id` (base URL `https://open.larksuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

