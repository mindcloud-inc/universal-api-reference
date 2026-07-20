# Jira Software Cloud: Get Comments

Retrieves issue comments from Jira Software Cloud.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-comments?connectionId=$CONNECTION_ID&cloudId=string&issueIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "issueIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-comments?${params}`, {
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
| `issueIdOrKey` | string | yes | Issue ID or key such as PROJ-123. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {
          "author": {
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
          "id": "string",
          "updated": "2026-05-07T12:00:00.000Z"
        }
      ],
      "maxResults": 1,
      "startAt": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments[].author.displayName` | string |  |
| `comments[].author.emailAddress` | string |  |
| `comments[].body.content[].content[].text` | string |  |
| `comments[].id` | string |  |
| `comments[].updated` | date |  |
| `maxResults` | number |  |
| `startAt` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comments.md) for the provider-specific parameters and requirements.

