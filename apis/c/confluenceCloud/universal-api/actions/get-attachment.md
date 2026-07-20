# Confluence: Get Attachment

Retrieves an existing attachment from Confluence.

```
GET https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-attachment?connectionId=$CONNECTION_ID&cloudId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-attachment?${params}`, {
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
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | string | yes | ID of the attachment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdAt": "string",
      "downloadLink": "https://example.com",
      "fileId": "string",
      "fileSize": 1,
      "id": "string",
      "Links": {
        "base": "https://example.com",
        "download": "https://example.com",
        "webui": "https://example.com"
      },
      "mediaType": "string",
      "mediaTypeDescription": {},
      "pageId": "string",
      "status": "string",
      "title": "string",
      "version": {
        "authorId": "string",
        "createdAt": "string",
        "message": "string",
        "minorEdit": true,
        "number": 1
      },
      "webuiLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdAt` | string |  |
| `downloadLink` | string |  |
| `fileId` | string |  |
| `fileSize` | number |  |
| `id` | string |  |
| `Links.base` | string |  |
| `Links.download` | string |  |
| `Links.webui` | string |  |
| `mediaType` | string |  |
| `mediaTypeDescription` | object |  |
| `pageId` | string |  |
| `status` | string |  |
| `title` | string |  |
| `version.authorId` | string |  |
| `version.createdAt` | string |  |
| `version.message` | string |  |
| `version.minorEdit` | boolean |  |
| `version.number` | number |  |
| `webuiLink` | string |  |

## Native endpoint

Through the native Confluence API, this operation is `GET /ex/confluence/:cloudId/wiki/api/v2/attachments/:id` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment.md) for the provider-specific parameters and requirements.

