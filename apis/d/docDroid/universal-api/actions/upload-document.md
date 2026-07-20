# DocDroid: Upload Document

Uploads a new document to DocDroid.

```
POST https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/upload-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocDroid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/upload-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/upload-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The file to upload. |
| `name` | string | no | Optional display name for the document. |
| `visibility` | list | no | Set the document visibility. One of: `password`, `private`, `public`. Default: `public`. |
| `type` | list | no | Optional document type. One of: `document`, `presentation`. |
| `password` | string | no | Optional password when visibility is set to password. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowDownload` | boolean | no | Whether downloads are allowed. |
| `allowSearchEnginesIndex` | boolean | no | Whether search engines may index the document. |
| `allowCopyText` | boolean | no | Whether copying text is allowed. |
| `allowEmbed` | list | no | Set embed permissions for the document. One of: `any`, `none`, `whitelist`. |
| `allowEmbedDomains[]` | array<string> | no | Optional list of domains allowed to embed the document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowAiChat": true,
      "allowCopyText": true,
      "allowDownload": true,
      "allowEmbed": "string",
      "allowSearchEnginesIndex": true,
      "created": "2026-05-07T12:00:00.000Z",
      "downloads": 1,
      "ext": "string",
      "filename": "Ava Chen",
      "hash": "string",
      "id": "string",
      "links": [
        {
          "rel": "https://example.com",
          "type": "https://example.com",
          "uri": "https://example.com"
        }
      ],
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "user": {
        "id": 1
      },
      "views": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowAiChat` | boolean |  |
| `allowCopyText` | boolean |  |
| `allowDownload` | boolean |  |
| `allowEmbed` | string |  |
| `allowSearchEnginesIndex` | boolean |  |
| `created` | date |  |
| `downloads` | number |  |
| `ext` | string |  |
| `filename` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `links` | array<object> |  |
| `links[].rel` | string |  |
| `links[].type` | string |  |
| `links[].uri` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `user` | object |  |
| `user.id` | number |  |
| `views` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native DocDroid API, this operation is `POST /document` (base URL `https://www.docdroid.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document.md) for the provider-specific parameters and requirements.

