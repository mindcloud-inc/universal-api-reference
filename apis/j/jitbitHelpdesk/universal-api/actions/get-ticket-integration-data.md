# Jitbit Helpdesk: Get Ticket Integration Data



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-ticket-integration-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-ticket-integration-data?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-ticket-integration-data?${params}`, {
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
| `id` | number | yes | Jitbit ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asanaTaskUrl": "https://example.com",
      "basecampTodoUrl": "https://example.com",
      "bitbucketIssueUrl": "https://example.com",
      "gitHubIssueUrl": "https://example.com",
      "gitLabIssueUrl": "https://example.com",
      "harvestProjectUrl": "https://example.com",
      "jiraIssueUrl": "https://example.com",
      "trelloCardUrl": "https://example.com",
      "vsoWorkItemUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asanaTaskUrl` | string | Linked Asana task URL. |
| `basecampTodoUrl` | string | Linked Basecamp todo URL. |
| `bitbucketIssueUrl` | string | Linked Bitbucket issue URL. |
| `gitHubIssueUrl` | string | Linked GitHub issue URL. |
| `gitLabIssueUrl` | string | Linked GitLab issue URL. |
| `harvestProjectUrl` | string | Linked Harvest project URL. |
| `jiraIssueUrl` | string | Linked Jira issue URL. |
| `trelloCardUrl` | string | Linked Trello card URL. |
| `vsoWorkItemUrl` | string | Linked Azure DevOps work item URL. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /TicketIntegrationData` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-integration-data.md) for the provider-specific parameters and requirements.

