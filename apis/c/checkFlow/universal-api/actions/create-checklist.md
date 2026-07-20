# CheckFlow: Create Checklist



```
POST https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-checklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateKey": "0e7ad584-7788-4ab1-95a6-ca0a5b444cbb",
  "checklistName": "MindCloud API Smoke Test"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-checklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateKey": "0e7ad584-7788-4ab1-95a6-ca0a5b444cbb",
    "checklistName": "MindCloud API Smoke Test"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateKey` | string | yes | The key of the template the checklist is derived from. Example: `0e7ad584-7788-4ab1-95a6-ca0a5b444cbb`. |
| `checklistName` | string | yes | The name for the new checklist. Example: `MindCloud API Smoke Test`. |

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

Through the native CheckFlow API, this operation is `POST /api/checklist` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checklist.md) for the provider-specific parameters and requirements.

