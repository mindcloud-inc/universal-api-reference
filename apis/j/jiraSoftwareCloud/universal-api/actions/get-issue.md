# Jira Software Cloud: Get Issue

Retrieves an issue from Jira Software Cloud.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-issue?connectionId=$CONNECTION_ID&cloudId=string&issueIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "issueIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-issue?${params}`, {
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
      "fields": {
        "assignee": {
          "accountId": "string",
          "displayName": "Ava Chen"
        },
        "created": "2026-05-07T12:00:00.000Z",
        "issuetype": {
          "name": "Ava Chen"
        },
        "priority": {
          "name": "Ava Chen"
        },
        "project": {
          "key": "string",
          "name": "Ava Chen"
        },
        "reporter": {
          "accountId": "string",
          "displayName": "Ava Chen"
        },
        "status": {
          "name": "Ava Chen"
        },
        "summary": "string",
        "updated": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields.assignee.accountId` | string |  |
| `fields.assignee.displayName` | string |  |
| `fields.created` | date |  |
| `fields.issuetype.name` | string |  |
| `fields.priority.name` | string |  |
| `fields.project.key` | string |  |
| `fields.project.name` | string |  |
| `fields.reporter.accountId` | string |  |
| `fields.reporter.displayName` | string |  |
| `fields.status.name` | string |  |
| `fields.summary` | string |  |
| `fields.updated` | date |  |
| `id` | string |  |
| `key` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue.md) for the provider-specific parameters and requirements.

