# Smartcat: Create Project

Creates a new project in Smartcat.

```
POST https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | object | yes | JSON object describing the project to create. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "assignmentMode": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "description": "string",
      "documents": [
        {}
      ],
      "externalTag": "string",
      "id": "string",
      "managers": [
        {}
      ],
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "sourceLanguage": "string",
      "sourceLanguageId": 1,
      "specializations": [
        {}
      ],
      "status": "string",
      "statusModificationDate": "2026-05-07T12:00:00.000Z",
      "targetLanguages": [
        "string"
      ],
      "vendors": [
        {}
      ],
      "workflowStages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Owning Smartcat account ID |
| `assignmentMode` | string | Assignment mode |
| `creationDate` | date | Project creation timestamp |
| `customFields` | object | Custom fields |
| `description` | string | Project description |
| `documents` | array<object> | Project documents |
| `externalTag` | string | External system tag |
| `id` | string | Project ID |
| `managers` | array<object> | Project managers |
| `modificationDate` | date | Project modification timestamp |
| `name` | string | Project name |
| `sourceLanguage` | string | Source language code |
| `sourceLanguageId` | number | Source language numeric ID |
| `specializations` | array<object> | Project specializations |
| `status` | string | Project status |
| `statusModificationDate` | date | Project status modification timestamp |
| `targetLanguages` | array<string> | Configured target language codes |
| `vendors` | array<object> | Assigned vendors |
| `workflowStages` | array<object> | Workflow stages |

## Native endpoint

Through the native Smartcat API, this operation is `POST /api/integration/v1/project/create` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

