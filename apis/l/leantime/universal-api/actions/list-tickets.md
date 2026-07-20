# Leantime: List Tickets



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-tickets?connectionId=$CONNECTION_ID&params.searchCriteria.currentProject=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.searchCriteria.currentProject": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-tickets?${params}`, {
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
| `params.searchCriteria.currentProject` | number | yes | List tickets for this project. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.searchCriteria.orderBy` | string | no | Optional ticket sort field. Default: `date`. |
| `params.searchCriteria.status` | string | no | Optional status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorFirstname": "Ava",
      "authorId": 1,
      "authorLastname": "Chen",
      "authorProfileId": "string",
      "bookedHours": "string",
      "clientId": {},
      "clientName": {},
      "commentCount": 1,
      "date": "string",
      "dateToFinish": "string",
      "dependingTicketId": 1,
      "description": "string",
      "editFrom": "string",
      "editorFirstname": {},
      "editorId": "string",
      "editorLastname": {},
      "editorProfileId": {},
      "editTo": "string",
      "fileCount": 1,
      "headline": "string",
      "hourRemaining": 1,
      "id": 1,
      "milestoneColor": "string",
      "milestoneHeadline": {},
      "milestoneid": 1,
      "parentHeadline": {},
      "planHours": 1,
      "priority": "string",
      "projectId": 1,
      "projectName": "Ava Chen",
      "sortindex": {},
      "sprint": 1,
      "sprintName": {},
      "status": 1,
      "statusLabel": "string",
      "storypoints": 1,
      "subtaskCount": 1,
      "tags": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorFirstname` | string |  |
| `authorId` | number |  |
| `authorLastname` | string |  |
| `authorProfileId` | string |  |
| `bookedHours` | string |  |
| `clientId` | object |  |
| `clientName` | object |  |
| `commentCount` | number |  |
| `date` | string |  |
| `dateToFinish` | string |  |
| `dependingTicketId` | number |  |
| `description` | string |  |
| `editFrom` | string |  |
| `editorFirstname` | object |  |
| `editorId` | string |  |
| `editorLastname` | object |  |
| `editorProfileId` | object |  |
| `editTo` | string |  |
| `fileCount` | number |  |
| `headline` | string |  |
| `hourRemaining` | number |  |
| `id` | number |  |
| `milestoneColor` | string |  |
| `milestoneHeadline` | object |  |
| `milestoneid` | number |  |
| `parentHeadline` | object |  |
| `planHours` | number |  |
| `priority` | string |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `sortindex` | object |  |
| `sprint` | number |  |
| `sprintName` | object |  |
| `status` | number |  |
| `statusLabel` | string |  |
| `storypoints` | number |  |
| `subtaskCount` | number |  |
| `tags` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

