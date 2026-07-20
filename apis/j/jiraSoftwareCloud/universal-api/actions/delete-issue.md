# Jira Software Cloud: Delete Issue

Deletes an existing issue from Jira Software Cloud.

```
DELETE https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/delete-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/delete-issue?connectionId=$CONNECTION_ID&cloudId=string&issueIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "issueIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/delete-issue?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jira Software Cloud API returns.

## Native endpoint

Through the native Jira Software Cloud API, this operation is `DELETE /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-issue.md) for the provider-specific parameters and requirements.

