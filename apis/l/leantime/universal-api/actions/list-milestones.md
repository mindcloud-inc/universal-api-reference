# Leantime: List Milestones



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-milestones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-milestones?connectionId=$CONNECTION_ID&params.searchCriteria.currentProject=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.searchCriteria.currentProject": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-milestones?${params}`, {
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
| `params.searchCriteria.currentProject` | number | yes | List milestones for this project. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.sortBy` | string | no | Milestone sort mode. Default: `standard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptanceCriteria": "string",
      "allTickets": {},
      "bookedHours": {},
      "clientName": {},
      "collaborators": {},
      "date": "string",
      "dateToFinish": "string",
      "dependingTicketId": 1,
      "description": "string",
      "doneTickets": {},
      "editFrom": "string",
      "editorFirstname": "Ava",
      "editorId": "string",
      "editorLastname": "Chen",
      "editorProfileId": "string",
      "editTo": "string",
      "headline": "string",
      "hourRemaining": 1,
      "id": 1,
      "milestoneColor": "string",
      "milestoneHeadline": "string",
      "milestoneid": 1,
      "modified": {},
      "parentHeadline": "string",
      "percentDone": {},
      "planHours": 1,
      "priority": "string",
      "projectDescription": {},
      "projectId": 1,
      "projectName": "Ava Chen",
      "sortIndex": 1,
      "sprint": 1,
      "status": 1,
      "storypoints": 1,
      "tags": "string",
      "timeFrom": {},
      "timelineDate": "string",
      "timelineDateToFinish": "string",
      "timeTo": {},
      "timeToFinish": {},
      "type": "string",
      "url": {},
      "userFirstname": "Ava",
      "userId": 1,
      "userLastname": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptanceCriteria` | string |  |
| `allTickets` | object |  |
| `bookedHours` | object |  |
| `clientName` | object |  |
| `collaborators` | object |  |
| `date` | string |  |
| `dateToFinish` | string |  |
| `dependingTicketId` | number |  |
| `description` | string |  |
| `doneTickets` | object |  |
| `editFrom` | string |  |
| `editorFirstname` | string |  |
| `editorId` | string |  |
| `editorLastname` | string |  |
| `editorProfileId` | string |  |
| `editTo` | string |  |
| `headline` | string |  |
| `hourRemaining` | number |  |
| `id` | number |  |
| `milestoneColor` | string |  |
| `milestoneHeadline` | string |  |
| `milestoneid` | number |  |
| `modified` | object |  |
| `parentHeadline` | string |  |
| `percentDone` | object |  |
| `planHours` | number |  |
| `priority` | string |  |
| `projectDescription` | object |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `sortIndex` | number |  |
| `sprint` | number |  |
| `status` | number |  |
| `storypoints` | number |  |
| `tags` | string |  |
| `timeFrom` | object |  |
| `timelineDate` | string |  |
| `timelineDateToFinish` | string |  |
| `timeTo` | object |  |
| `timeToFinish` | object |  |
| `type` | string |  |
| `url` | object |  |
| `userFirstname` | string |  |
| `userId` | number |  |
| `userLastname` | string |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-milestones.md) for the provider-specific parameters and requirements.

