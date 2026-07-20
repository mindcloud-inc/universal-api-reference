# CheckFlow: Get Checklist Details



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-checklist-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-checklist-details?connectionId=$CONNECTION_ID&limit=25&offset=0&templateKey=0e7ad584-7788-4ab1-95a6-ca0a5b444cbb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "templateKey": "0e7ad584-7788-4ab1-95a6-ca0a5b444cbb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-checklist-details?${params}`, {
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
| `templateKey` | string | yes | The key of the template the checklist is derived from. Example: `0e7ad584-7788-4ab1-95a6-ca0a5b444cbb`. |
| `checklistKey` | string | no | The key of the checklist to return. Example: `9fd97cb0-e9d4-4ee0-8d9f-abc123456789`. |
| `checklistName` | string | no | Full or partial checklist name to search for. Example: `MindCloud`. |
| `tag` | string | no | Full or partial tag name to filter by. Example: `urgent`. |
| `status` | string | no | Checklist status filter. Values include ALL, SCHEDULED, INPROGRESS, and COMPLETE. Example: `ALL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checklistCreatedByEmail": "ava@example.com",
      "checklistCreatedByName": "Ava Chen",
      "checklistEndDateTime": "2026-05-07T12:00:00.000Z",
      "checklistId": 1,
      "checklistIsArchived": true,
      "checklistIsShared": true,
      "checklistKey": "string",
      "checklistName": "Ava Chen",
      "checklistScheduledDateTime": "2026-05-07T12:00:00.000Z",
      "checklistSharedUrl": "https://example.com",
      "checklistStartDateTime": "2026-05-07T12:00:00.000Z",
      "checklistUrl": "https://example.com",
      "tags": [
        {}
      ],
      "tasks": [
        {}
      ],
      "template": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checklistCreatedByEmail` | string |  |
| `checklistCreatedByName` | string |  |
| `checklistEndDateTime` | date |  |
| `checklistId` | number |  |
| `checklistIsArchived` | boolean |  |
| `checklistIsShared` | boolean |  |
| `checklistKey` | string |  |
| `checklistName` | string |  |
| `checklistScheduledDateTime` | date |  |
| `checklistSharedUrl` | string |  |
| `checklistStartDateTime` | date |  |
| `checklistUrl` | string |  |
| `tags` | array<object> |  |
| `tasks` | array<object> |  |
| `template` | object |  |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/checklist/details` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-checklist-details.md) for the provider-specific parameters and requirements.

