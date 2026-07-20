# CheckFlow: Create Checklist With Parameters



```
POST https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-checklist-with-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-checklist-with-parameters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateKey": "0e7ad584-7788-4ab1-95a6-ca0a5b444cbb",
  "checklistName": "MindCloud Parameterized Smoke Test",
  "parameters[].parameterName": "Invoice Number",
  "parameters[].parameterValue": "INV-00123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-checklist-with-parameters', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateKey": "0e7ad584-7788-4ab1-95a6-ca0a5b444cbb",
    "checklistName": "MindCloud Parameterized Smoke Test",
    "parameters[].parameterName": "Invoice Number",
    "parameters[].parameterValue": "INV-00123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateKey` | string | yes | The key of the template to create the checklist from. Example: `0e7ad584-7788-4ab1-95a6-ca0a5b444cbb`. |
| `checklistName` | string | yes | The name for the new checklist. Example: `MindCloud Parameterized Smoke Test`. |
| `parameters[]` | array<object> | no | A list of parameter name and value pairs to set on creation. Example: `[object Object]`. |
| `parameters[].parameterName` | string | yes | The name of the template parameter. Example: `Invoice Number`. |
| `parameters[].parameterValue` | string | yes | The value to assign to the template parameter. Example: `INV-00123`. |

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

Through the native CheckFlow API, this operation is `POST /api/checklist/create-with-parameters` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checklist-with-parameters.md) for the provider-specific parameters and requirements.

