# DocDroid: Get Document

Retrieves a document from DocDroid by ID.

```
GET https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocDroid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/get-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/get-document?${params}`, {
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
| `id` | string | yes | The ID of the document. |

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

Through the native DocDroid API, this operation is `GET /document/:id` (base URL `https://www.docdroid.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

