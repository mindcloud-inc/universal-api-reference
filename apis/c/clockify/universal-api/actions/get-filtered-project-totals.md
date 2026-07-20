# Clockify: Get Filtered Project Totals

Retrieves filtered project totals from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-filtered-project-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-filtered-project-totals?connectionId=$CONNECTION_ID&end=2026-05-07T12%3A00%3A00.000Z&start=2026-05-07T12%3A00%3A00.000Z&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "2026-05-07T12:00:00.000Z",
  "start": "2026-05-07T12:00:00.000Z",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-filtered-project-totals?${params}`, {
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
| `end` | date | yes |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `search` | string | no |  |
| `start` | date | yes |  |
| `statusFilter` | list | no | One of: `ALL`, `PUBLISHED`, `UNPUBLISHED`. |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].assignments[]` | array<object> |  |
| `items[].assignments[].date` | date |  |
| `items[].assignments[].hasAssignment` | boolean |  |
| `items[].clientName` | string |  |
| `items[].milestones[]` | array<object> |  |
| `items[].milestones[].date` | date |  |
| `items[].milestones[].id` | string |  |
| `items[].milestones[].name` | string |  |
| `items[].milestones[].projectId` | string |  |
| `items[].milestones[].workspaceId` | string |  |
| `items[].projectArchived` | boolean |  |
| `items[].projectBillable` | boolean |  |
| `items[].projectColor` | string |  |
| `items[].projectId` | string |  |
| `items[].projectName` | string |  |
| `items[].totalHours` | number |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/scheduling/assignments/projects/totals` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filtered-project-totals.md) for the provider-specific parameters and requirements.

