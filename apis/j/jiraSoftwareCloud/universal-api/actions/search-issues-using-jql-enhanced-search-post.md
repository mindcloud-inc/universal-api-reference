# Jira Software Cloud: Search Issues Using JQL Enhanced Search (POST)

Finds issues in Jira Software Cloud using JQL.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/search-issues-using-jql-enhanced-search-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/search-issues-using-jql-enhanced-search-post?connectionId=$CONNECTION_ID&cloudId=string&jql=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "jql": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/search-issues-using-jql-enhanced-search-post?${params}`, {
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
| `jql` | string | yes | JQL query string. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[]` | array<string> | no | Optional Jira issue fields to include in each search result. |
| `maxResults` | number | no | Optional maximum number of issues to return. |
| `nextPageToken` | string | no | Optional pagination token returned by Jira enhanced search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isLast": true,
      "issues": [
        {
          "fields": {
            "issuetype": {
              "iconUrl": "https://example.com",
              "name": "Ava Chen"
            },
            "project": {
              "key": "string",
              "name": "Ava Chen"
            },
            "status": {
              "name": "Ava Chen"
            },
            "summary": "string"
          },
          "id": "string",
          "key": "string"
        }
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isLast` | boolean |  |
| `issues[].fields.issuetype.iconUrl` | string |  |
| `issues[].fields.issuetype.name` | string |  |
| `issues[].fields.project.key` | string |  |
| `issues[].fields.project.name` | string |  |
| `issues[].fields.status.name` | string |  |
| `issues[].fields.summary` | string |  |
| `issues[].id` | string |  |
| `issues[].key` | string |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `POST /ex/jira/:cloudId/rest/api/3/search/jql` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-issues-using-jql-enhanced-search-post.md) for the provider-specific parameters and requirements.

