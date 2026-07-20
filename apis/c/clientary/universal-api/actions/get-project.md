# Clientary: Get Project

Retrieves a project from Clientary by project ID.

```
GET https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | The Clientary project ID. |

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

Through the native Clientary API, this operation is `GET /projects/:id` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

