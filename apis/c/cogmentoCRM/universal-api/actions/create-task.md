# Cogmento CRM: Create Task



```
POST https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cogmento CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The title of the task. |
| `description` | string | no | A description of the task. |
| `dueDate` | date | no | The task deadline, formatted YYYY-MM-DD. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedTo[]` | array<object> | no | Array of assignee user reference objects. |
| `deal` | object | no | Deal reference object associated with the task. |
| `contact` | object | no | Contact reference object associated with the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": {
        "private": true
      },
      "accountId": "string",
      "acl": [
        {}
      ],
      "alerts": [
        {}
      ],
      "assignedTo": [
        {}
      ],
      "auxId": "string",
      "auxSource": "string",
      "auxSourceName": "Ava Chen",
      "calls": [
        {}
      ],
      "case": {},
      "cases": [
        {}
      ],
      "closeDate": "string",
      "company": {},
      "contact": {},
      "createdAt": "string",
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "notificationOptIn": true
      },
      "deal": {},
      "description": "string",
      "documents": [
        {}
      ],
      "dueDate": "string",
      "events": [
        {}
      ],
      "flags": {
        "callAssigned": true,
        "caseAssigned": true,
        "emailReceived": true,
        "eventAssigned": true,
        "new": true,
        "taskAssigned": true,
        "updated": true
      },
      "id": "string",
      "lastModified": "string",
      "notes": [
        {}
      ],
      "private": true,
      "rating": 1,
      "tags": [
        {}
      ],
      "templateId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access.private` | boolean |  |
| `accountId` | string |  |
| `acl` | array<object> |  |
| `alerts` | array<object> |  |
| `assignedTo` | array<object> |  |
| `auxId` | string |  |
| `auxSource` | string |  |
| `auxSourceName` | string |  |
| `calls` | array<object> |  |
| `case` | object |  |
| `cases` | array<object> |  |
| `closeDate` | string |  |
| `company` | object |  |
| `contact` | object |  |
| `createdAt` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.notificationOptIn` | boolean |  |
| `deal` | object |  |
| `description` | string |  |
| `documents` | array<object> |  |
| `dueDate` | string |  |
| `events` | array<object> |  |
| `flags.callAssigned` | boolean |  |
| `flags.caseAssigned` | boolean |  |
| `flags.emailReceived` | boolean |  |
| `flags.eventAssigned` | boolean |  |
| `flags.new` | boolean |  |
| `flags.taskAssigned` | boolean |  |
| `flags.updated` | boolean |  |
| `id` | string |  |
| `lastModified` | string |  |
| `notes` | array<object> |  |
| `private` | boolean |  |
| `rating` | number |  |
| `tags` | array<object> |  |
| `templateId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Cogmento CRM API, this operation is `POST /tasks/` (base URL `https://api.freecrm.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

