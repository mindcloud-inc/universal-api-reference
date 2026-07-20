# Confluence: Create Blog Post

Creates a new blog post in Confluence.

```
POST https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/create-blog-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/create-blog-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/create-blog-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "body": {
        "storage": {
          "representation": "string",
          "value": "string"
        }
      },
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
| `body.storage.representation` | string |  |
| `body.storage.value` | string |  |
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

Through the native Confluence API, this operation is `POST /ex/confluence/:cloudId/wiki/api/v2/blogposts` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blog-post.md) for the provider-specific parameters and requirements.

