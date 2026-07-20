# Confluence: Update Footer Comment

Updates an existing footer comment in Confluence.

```
PUT https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-footer-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-footer-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudId": "string",
  "commentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-footer-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudId": "string",
    "commentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `commentId` | string | yes | ID of the footer comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {
        "storage": {
          "representation": "string",
          "value": "string"
        }
      },
      "id": "string",
      "Links": {
        "base": "https://example.com",
        "webui": "https://example.com"
      },
      "pageId": "string",
      "resolutionStatus": "string",
      "status": "string",
      "title": "string",
      "version": {
        "authorId": "string",
        "createdAt": "string",
        "message": "string",
        "minorEdit": true,
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
| `body.storage.representation` | string |  |
| `body.storage.value` | string |  |
| `id` | string |  |
| `Links.base` | string |  |
| `Links.webui` | string |  |
| `pageId` | string |  |
| `resolutionStatus` | string |  |
| `status` | string |  |
| `title` | string |  |
| `version.authorId` | string |  |
| `version.createdAt` | string |  |
| `version.message` | string |  |
| `version.minorEdit` | boolean |  |
| `version.number` | number |  |

## Native endpoint

Through the native Confluence API, this operation is `PUT /ex/confluence/:cloudId/wiki/api/v2/footer-comments/:commentId` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-footer-comment.md) for the provider-specific parameters and requirements.

