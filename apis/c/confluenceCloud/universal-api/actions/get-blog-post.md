# Confluence: Get Blog Post

Retrieves a blog post from Confluence.

```
GET https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-blog-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-blog-post?connectionId=$CONNECTION_ID&cloudId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-blog-post?${params}`, {
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
| `id` | string | yes | ID of the Confluence blog post. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "createdAt": "string",
      "id": "string",
      "Links": {
        "base": "https://example.com",
        "editui": "https://example.com",
        "edituiv2": "https://example.com",
        "tinyui": "https://example.com",
        "webui": "https://example.com"
      },
      "spaceId": "string",
      "status": "string",
      "title": "string",
      "version": {
        "authorId": "string",
        "createdAt": "string",
        "message": "string",
        "minorEdit": true,
        "ncsStepVersion": "string",
        "number": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `Links.base` | string |  |
| `Links.editui` | string |  |
| `Links.edituiv2` | string |  |
| `Links.tinyui` | string |  |
| `Links.webui` | string |  |
| `spaceId` | string |  |
| `status` | string |  |
| `title` | string |  |
| `version.authorId` | string |  |
| `version.createdAt` | string |  |
| `version.message` | string |  |
| `version.minorEdit` | boolean |  |
| `version.ncsStepVersion` | string |  |
| `version.number` | number |  |

## Native endpoint

Through the native Confluence API, this operation is `GET /ex/confluence/:cloudId/wiki/api/v2/blogposts/:id` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blog-post.md) for the provider-specific parameters and requirements.

