# Feishu Drive: Get File Metadata

Retrieves file metadata from Feishu Drive.

```
GET https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/get-file-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/get-file-metadata?connectionId=$CONNECTION_ID&requestDocs%5B%5D=%5Bobject%20Object%5D&requestDocs%5B%5D.docToken=string&requestDocs%5B%5D.docType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestDocs[]": "[object Object]",
  "requestDocs[].docToken": "string",
  "requestDocs[].docType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/get-file-metadata?${params}`, {
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
| `requestDocs[]` | array<object> | yes | Array of requested Drive docs. Each item must include doc_token and doc_type. |
| `requestDocs[].docToken` | string | yes | Drive doc token for each requested document. |
| `requestDocs[].docType` | string | yes | Drive doc type for each requested document, such as file or docx. |
| `withUrl` | boolean | no | Whether to include the file URL in the metadata response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "metas": [
          {
            "create_time": "string",
            "doc_token": "string",
            "doc_type": "string",
            "latest_modify_time": "string",
            "latest_modify_user": "string",
            "owner_id": "string",
            "request_doc_info": {
              "doc_token": "string",
              "doc_type": "string"
            },
            "sec_label_name": "Ava Chen",
            "title": "string",
            "url": "https://example.com"
          }
        ]
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
| `code` | number |  |
| `data.metas[].create_time` | string |  |
| `data.metas[].doc_token` | string |  |
| `data.metas[].doc_type` | string |  |
| `data.metas[].latest_modify_time` | string |  |
| `data.metas[].latest_modify_user` | string |  |
| `data.metas[].owner_id` | string |  |
| `data.metas[].request_doc_info.doc_token` | string |  |
| `data.metas[].request_doc_info.doc_type` | string |  |
| `data.metas[].sec_label_name` | string |  |
| `data.metas[].title` | string |  |
| `data.metas[].url` | string |  |
| `msg` | string |  |

## Native endpoint

Through the native Feishu Drive API, this operation is `POST /drive/v1/metas/batch_query` (base URL `https://open.feishu.cn/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-metadata.md) for the provider-specific parameters and requirements.

