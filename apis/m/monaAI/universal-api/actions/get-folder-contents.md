# Mona AI: Get Folder Contents

Retrieves folder contents from Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-folder-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-folder-contents?connectionId=$CONNECTION_ID&folderId=string&permission=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string",
  "permission": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-folder-contents?${params}`, {
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
| `folderId` | string | yes | Knowledge folder identifier to inspect. |
| `includeFiles` | boolean | no | Whether to include files in folder contents. |
| `includeSubfolders` | boolean | no | Whether to include nested folders. |
| `permission` | string | yes | Mona permission string required by the folder contents endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contents": [
          {}
        ],
        "folderPath": [
          "string"
        ]
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Folder content result container. |
| `data.contents` | array<object> | Folder content entries. |
| `data.folderPath` | array<string> | Path segments for the folder. |
| `message` | string | Folder content retrieval status message. |
| `success` | boolean | Whether Mona retrieved the folder contents. |

## Native endpoint

Through the native Mona AI API, this operation is `POST /companyKnowledge/getFolderContents` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder-contents.md) for the provider-specific parameters and requirements.

