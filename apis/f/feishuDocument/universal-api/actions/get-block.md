# Feishu Document: Get Block

Retrieves a specific block from a Feishu document.

```
GET https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Document `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-block?connectionId=$CONNECTION_ID&blockId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blockId": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-block?${params}`, {
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
| `blockId` | string | yes | The unique block id within the document. |
| `documentId` | string | yes | The unique document token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "block": {
          "block_id": "string",
          "block_type": 1,
          "parent_id": "string"
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
| `data.block.block_id` | string | Block id. |
| `data.block.block_type` | number | Block type code. |
| `data.block.parent_id` | string | Parent block id. |
| `msg` | string | Provider status message. |

## Native endpoint

Through the native Feishu Document API, this operation is `GET /open-apis/docx/v1/documents/:document_id/blocks/:block_id` (base URL `https://open.larksuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block.md) for the provider-specific parameters and requirements.

