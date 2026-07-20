# Cogmento CRM: Create Deal



```
POST https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cogmento CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-deal', {
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
| `title` | string | yes | The title of the deal. |
| `description` | string | no | A description of the deal. |
| `tags[]` | array<string> | no | Tags associated with the deal. Accepts multiple values as an array. |
| `closeDate` | date | no | Date the deal was completed, formatted YYYY-MM-DD. |
| `amount` | number | no | Final deal value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedTo[]` | array<object> | no | Array of assignee user reference objects. |
| `products[]` | array<object> | no | Array of product reference objects associated with the deal. |

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
      "amount": 1,
      "assignedTo": [
        {}
      ],
      "auxId": "string",
      "auxSource": "string",
      "auxSourceName": "Ava Chen",
      "calls": [
        {}
      ],
      "cases": [
        {}
      ],
      "closed": true,
      "closeDate": "string",
      "company": {},
      "contacts": [
        {}
      ],
      "createdAt": "string",
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "notificationOptIn": true
      },
      "dealProducts": [
        {}
      ],
      "description": "string",
      "documents": [
        {}
      ],
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
      "invoices": [
        {}
      ],
      "lastModified": "string",
      "notes": [
        {}
      ],
      "private": true,
      "products": [
        {}
      ],
      "rating": 1,
      "summary": {
        "totalValue": 1
      },
      "tags": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "tasks": [
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
| `amount` | number |  |
| `assignedTo` | array<object> |  |
| `auxId` | string |  |
| `auxSource` | string |  |
| `auxSourceName` | string |  |
| `calls` | array<object> |  |
| `cases` | array<object> |  |
| `closed` | boolean |  |
| `closeDate` | string |  |
| `company` | object |  |
| `contacts` | array<object> |  |
| `createdAt` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.notificationOptIn` | boolean |  |
| `dealProducts` | array<object> |  |
| `description` | string |  |
| `documents` | array<object> |  |
| `events` | array<object> |  |
| `flags.callAssigned` | boolean |  |
| `flags.caseAssigned` | boolean |  |
| `flags.emailReceived` | boolean |  |
| `flags.eventAssigned` | boolean |  |
| `flags.new` | boolean |  |
| `flags.taskAssigned` | boolean |  |
| `flags.updated` | boolean |  |
| `id` | string |  |
| `invoices` | array<object> |  |
| `lastModified` | string |  |
| `notes` | array<object> |  |
| `private` | boolean |  |
| `products` | array<object> |  |
| `rating` | number |  |
| `summary.totalValue` | number |  |
| `tags` | array<object> |  |
| `tags[].id` | string |  |
| `tags[].name` | string |  |
| `tasks` | array<object> |  |
| `templateId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Cogmento CRM API, this operation is `POST /deals/` (base URL `https://api.freecrm.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

