# Clientary: Create Project

Creates a new project in Clientary.

```
POST https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project.name": "Ava Chen",
  "project.rate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project.name": "Ava Chen",
    "project.rate": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project.budgetType` | string | no | The project budget type. |
| `project.name` | string | yes | The project name. |
| `project.number` | string | no | Optional unique project number. |
| `project.projectType` | string | no | The project type. |
| `project.rate` | number | yes | The project hourly rate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billedPercentage": 1,
      "budget": 1,
      "budgetEnabled": true,
      "budgetPercentage": 1,
      "budgetType": 1,
      "comments": [
        {}
      ],
      "cost": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditPercentage": 1,
      "credits": 1,
      "currencyCode": "string",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "note": "string",
      "number": "string",
      "parentTemplateId": 1,
      "parentTemplateUpdatedAt": "2026-05-07T12:00:00.000Z",
      "projectType": 1,
      "rate": 1,
      "status": 1,
      "subcontracts": [
        {}
      ],
      "tasksCount": 1,
      "templateDescription": "string",
      "templateName": "Ava Chen",
      "title": "string",
      "todoTasksCount": 1,
      "type": "string",
      "unbilledAmount": 1,
      "unbilledCreditAmount": 1,
      "unbilledHours": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workedHours": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billedPercentage` | number |  |
| `budget` | number |  |
| `budgetEnabled` | boolean |  |
| `budgetPercentage` | number |  |
| `budgetType` | number |  |
| `comments` | array<object> |  |
| `cost` | number |  |
| `createdAt` | date |  |
| `creditPercentage` | number |  |
| `credits` | number |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `endDate` | date |  |
| `id` | number |  |
| `name` | string |  |
| `note` | string |  |
| `number` | string |  |
| `parentTemplateId` | number |  |
| `parentTemplateUpdatedAt` | date |  |
| `projectType` | number |  |
| `rate` | number |  |
| `status` | number |  |
| `subcontracts` | array<object> |  |
| `tasksCount` | number |  |
| `templateDescription` | string |  |
| `templateName` | string |  |
| `title` | string |  |
| `todoTasksCount` | number |  |
| `type` | string |  |
| `unbilledAmount` | number |  |
| `unbilledCreditAmount` | number |  |
| `unbilledHours` | number |  |
| `updatedAt` | date |  |
| `workedHours` | number |  |

## Native endpoint

Through the native Clientary API, this operation is `POST /projects` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

