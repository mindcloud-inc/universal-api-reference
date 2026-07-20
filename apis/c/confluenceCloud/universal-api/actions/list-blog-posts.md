# Confluence: List Blog Posts

Retrieves a list of blog posts from Confluence.

```
GET https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-blog-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-blog-posts?connectionId=$CONNECTION_ID&limit=25&offset=0&cloudId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "cloudId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-blog-posts?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "Links": {
        "base": "https://example.com"
      },
      "results": [
        {
          "authorId": "string",
          "createdAt": "string",
          "id": "string",
          "Links": {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Links.base` | string |  |
| `results[].authorId` | string |  |
| `results[].createdAt` | string |  |
| `results[].id` | string |  |
| `results[].Links.editui` | string |  |
| `results[].Links.edituiv2` | string |  |
| `results[].Links.tinyui` | string |  |
| `results[].Links.webui` | string |  |
| `results[].spaceId` | string |  |
| `results[].status` | string |  |
| `results[].title` | string |  |
| `results[].version.authorId` | string |  |
| `results[].version.createdAt` | string |  |
| `results[].version.message` | string |  |
| `results[].version.minorEdit` | boolean |  |
| `results[].version.ncsStepVersion` | string |  |
| `results[].version.number` | number |  |

## Native endpoint

Through the native Confluence API, this operation is `GET /ex/confluence/:cloudId/wiki/api/v2/blogposts` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-blog-posts.md) for the provider-specific parameters and requirements.

