# Jira Software Cloud: Get Comment

Retrieves a comment from Jira Software Cloud.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-comment?connectionId=$CONNECTION_ID&cloudId=string&id=string&issueIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "id": "string",
  "issueIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-comment?${params}`, {
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

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment/:id` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

