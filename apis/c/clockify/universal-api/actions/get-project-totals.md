# Clockify: Get Project Totals

Retrieves project totals for one project from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-project-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-project-totals?connectionId=$CONNECTION_ID&end=string&projectId=string&start=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "projectId": "string",
  "start": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-project-totals?${params}`, {
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
| `end` | string | yes |  |
| `projectId` | string | yes |  |
| `start` | string | yes |  |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignments": [
        [
          {}
        ]
      ],
      "clientName": "Ava Chen",
      "milestones": [
        [
          {}
        ]
      ],
      "projectArchived": true,
      "projectBillable": true,
      "projectColor": "string",
      "projectId": "string",
      "projectName": "Ava Chen",
      "totalHours": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignments[]` | array<object> |  |
| `assignments[].date` | date |  |
| `assignments[].hasAssignment` | boolean |  |
| `clientName` | string |  |
| `milestones[]` | array<object> |  |
| `milestones[].date` | date |  |
| `milestones[].id` | string |  |
| `milestones[].name` | string |  |
| `milestones[].projectId` | string |  |
| `milestones[].workspaceId` | string |  |
| `projectArchived` | boolean |  |
| `projectBillable` | boolean |  |
| `projectColor` | string |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `totalHours` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/scheduling/assignments/projects/totals/:projectId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-totals.md) for the provider-specific parameters and requirements.

