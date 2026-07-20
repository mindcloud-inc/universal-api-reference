# Jira Software Cloud: Assign Issue

Updates an issue assignee in Jira Software Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/assign-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/assign-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "cloudId": "string",
  "issueIdOrKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/assign-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "cloudId": "string",
    "issueIdOrKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Atlassian account ID to assign the issue to. |
| `cloudId` | string | yes | Jira cloud site ID returned by Accessible Resources. |
| `issueIdOrKey` | string | yes | Issue ID or key such as PROJ-123. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jira Software Cloud API returns.

## Native endpoint

Through the native Jira Software Cloud API, this operation is `PUT /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/assignee` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-issue.md) for the provider-specific parameters and requirements.

