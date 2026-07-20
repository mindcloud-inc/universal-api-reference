# Leantime: Get Ticket



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-ticket?connectionId=$CONNECTION_ID&params.id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-ticket?${params}`, {
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
| `params.id` | number | yes | The ticket ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptanceCriteria": "string",
      "allTickets": {},
      "bookedHours": {},
      "children": {},
      "clientName": {},
      "date": "string",
      "dateToFinish": "string",
      "dependingTicketId": 1,
      "description": "string",
      "doneTickets": {},
      "editFrom": "string",
      "editorFirstname": {},
      "editorId": "string",
      "editorLastname": {},
      "editorProfileId": {},
      "editTo": "string",
      "headline": "string",
      "hourRemaining": 1,
      "id": 1,
      "milestoneColor": {},
      "milestoneHeadline": {},
      "milestoneid": 1,
      "modified": {},
      "parentHeadline": {},
      "percentDone": {},
      "planHours": 1,
      "priority": "string",
      "projectDescription": "string",
      "projectId": 1,
      "projectName": "Ava Chen",
      "sortIndex": {},
      "sprint": 1,
      "status": 1,
      "storypoints": 1,
      "tags": "string",
      "timeFrom": {},
      "timelineDate": {},
      "timelineDateToFinish": {},
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
| `children` | object |  |
| `clientName` | object |  |
| `date` | string |  |
| `dateToFinish` | string |  |
| `dependingTicketId` | number |  |
| `description` | string |  |
| `doneTickets` | object |  |
| `editFrom` | string |  |
| `editorFirstname` | object |  |
| `editorId` | string |  |
| `editorLastname` | object |  |
| `editorProfileId` | object |  |
| `editTo` | string |  |
| `headline` | string |  |
| `hourRemaining` | number |  |
| `id` | number |  |
| `milestoneColor` | object |  |
| `milestoneHeadline` | object |  |
| `milestoneid` | number |  |
| `modified` | object |  |
| `parentHeadline` | object |  |
| `percentDone` | object |  |
| `planHours` | number |  |
| `priority` | string |  |
| `projectDescription` | string |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `sortIndex` | object |  |
| `sprint` | number |  |
| `status` | number |  |
| `storypoints` | number |  |
| `tags` | string |  |
| `timeFrom` | object |  |
| `timelineDate` | object |  |
| `timelineDateToFinish` | object |  |
| `timeTo` | object |  |
| `timeToFinish` | object |  |
| `type` | string |  |
| `url` | object |  |
| `userFirstname` | string |  |
| `userId` | number |  |
| `userLastname` | string |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

