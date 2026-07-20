# CheckFlow: Create Many Checklists



```
POST https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-many-checklists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-many-checklists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateKey": "0e7ad584-7788-4ab1-95a6-ca0a5b444cbb",
  "checklistNames[]": "MindCloud Batch Smoke A,MindCloud Batch Smoke B"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-many-checklists', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateKey": "0e7ad584-7788-4ab1-95a6-ca0a5b444cbb",
    "checklistNames[]": "MindCloud Batch Smoke A,MindCloud Batch Smoke B"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateKey` | string | yes | The key of the template to create checklists from. Example: `0e7ad584-7788-4ab1-95a6-ca0a5b444cbb`. |
| `checklistNames[]` | array<string> | yes | The names of the new checklists to create. Example: `MindCloud Batch Smoke A,MindCloud Batch Smoke B`. |

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
| `tasks` | array<object> |  |
| `template` | object |  |

## Native endpoint

Through the native CheckFlow API, this operation is `POST /api/checklist/create-many` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-many-checklists.md) for the provider-specific parameters and requirements.

