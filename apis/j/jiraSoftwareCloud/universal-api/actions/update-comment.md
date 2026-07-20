# Jira Software Cloud: Update Comment

Updates an existing comment in Jira Software Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/update-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/update-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "cloudId": "string",
  "id": "string",
  "issueIdOrKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/update-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "cloudId": "string",
    "id": "string",
    "issueIdOrKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Updated Atlassian Document Format comment body payload. |
| `cloudId` | string | yes | Jira cloud site ID returned by Accessible Resources. |
| `id` | string | yes | Comment ID. |
| `issueIdOrKey` | string | yes | Issue ID or key such as PROJ-123. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {
        "accountId": "string",
        "avatarUrls": {
          "48x48": "https://example.com"
        },
        "displayName": "Ava Chen",
        "emailAddress": "ava@example.com"
      },
      "body": {
        "content": [
          {
            "content": [
              {
                "text": "string"
              }
            ]
          }
        ]
      },
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "jsdPublic": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author.accountId` | string |  |
| `author.avatarUrls.48x48` | string |  |
| `author.displayName` | string |  |
| `author.emailAddress` | string |  |
| `body.content[].content[].text` | string |  |
| `created` | date |  |
| `id` | string |  |
| `jsdPublic` | boolean |  |
| `updated` | date |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `PUT /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment/:id` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-comment.md) for the provider-specific parameters and requirements.

