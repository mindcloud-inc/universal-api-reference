# Moco: Update Project



```
PUT https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddress` | string | no |  |
| `billingContactId` | string | no |  |
| `billingEmailCc` | string | no |  |
| `billingEmailTo` | string | no |  |
| `billingNotes` | string | no |  |
| `billingVariant` | string | no |  |
| `budget` | string | no |  |
| `budgetExpenses` | string | no |  |
| `budgetMonthly` | string | no |  |
| `coLeaderId` | string | no |  |
| `contactId` | string | no |  |
| `customerId` | string | no |  |
| `customProperties` | string | no |  |
| `dealId` | string | no |  |
| `finishDate` | string | no |  |
| `fixedPrice` | string | no |  |
| `hourlyRate` | string | no |  |
| `id` | number | yes |  |
| `identifier` | string | no |  |
| `info` | string | no |  |
| `leaderId` | string | no |  |
| `name` | string | no |  |
| `projectGroupId` | string | no |  |
| `retainer` | string | no |  |
| `retainerBillingDate` | string | no |  |
| `retainerBillingDescription` | string | no |  |
| `retainerBillingTitle` | string | no |  |
| `secondaryContactId` | string | no |  |
| `settingIncludeTimeReport` | string | no |  |
| `skipFavorite` | string | no |  |
| `startDate` | string | no |  |
| `tags` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "archivedOn": {},
      "billable": true,
      "billingAddress": "string",
      "billingContact": {},
      "billingEmailCc": {},
      "billingEmailTo": {},
      "billingNotes": "string",
      "billingVariant": "string",
      "budget": {},
      "budgetExpenses": 1,
      "budgetMonthly": {},
      "coLeader": {},
      "color": "string",
      "contact": {},
      "contracts": [
        [
          {}
        ]
      ],
      "createdAt": "string",
      "currency": "string",
      "customer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "customerReportUrl": {},
      "customProperties": {},
      "deal": {},
      "finishDate": {},
      "fixedPrice": true,
      "hourlyRate": 1,
      "id": 1,
      "identifier": "string",
      "info": "string",
      "labels": [
        [
          "string"
        ]
      ],
      "leader": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      },
      "name": "Ava Chen",
      "projectGroup": {},
      "retainer": true,
      "retainerBillingDate": 1,
      "retainerBillingDescription": {},
      "retainerBillingTitle": {},
      "secondaryContact": {},
      "settingIncludeTimeReport": true,
      "startDate": {},
      "tags": [
        [
          "string"
        ]
      ],
      "tasks": [
        [
          {}
        ]
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `archivedOn` | object |  |
| `billable` | boolean |  |
| `billingAddress` | string |  |
| `billingContact` | object |  |
| `billingEmailCc` | object |  |
| `billingEmailTo` | object |  |
| `billingNotes` | string |  |
| `billingVariant` | string |  |
| `budget` | object |  |
| `budgetExpenses` | number |  |
| `budgetMonthly` | object |  |
| `coLeader` | object |  |
| `color` | string |  |
| `contact` | object |  |
| `contracts[]` | array<object> |  |
| `contracts[].active` | boolean |  |
| `contracts[].billable` | boolean |  |
| `contracts[].budget` | object |  |
| `contracts[].firstname` | string |  |
| `contracts[].hourlyRate` | number |  |
| `contracts[].id` | number |  |
| `contracts[].lastname` | string |  |
| `contracts[].userId` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customer` | object |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customerReportUrl` | object |  |
| `customProperties` | object |  |
| `deal` | object |  |
| `finishDate` | object |  |
| `fixedPrice` | boolean |  |
| `hourlyRate` | number |  |
| `id` | number |  |
| `identifier` | string |  |
| `info` | string |  |
| `labels[]` | array<string> |  |
| `leader` | object |  |
| `leader.firstname` | string |  |
| `leader.id` | number |  |
| `leader.lastname` | string |  |
| `name` | string |  |
| `projectGroup` | object |  |
| `retainer` | boolean |  |
| `retainerBillingDate` | number |  |
| `retainerBillingDescription` | object |  |
| `retainerBillingTitle` | object |  |
| `secondaryContact` | object |  |
| `settingIncludeTimeReport` | boolean |  |
| `startDate` | object |  |
| `tags[]` | array<string> |  |
| `tasks[]` | array<object> |  |
| `tasks[].active` | boolean |  |
| `tasks[].billable` | boolean |  |
| `tasks[].budget` | object |  |
| `tasks[].description` | object |  |
| `tasks[].hourlyRate` | number |  |
| `tasks[].id` | number |  |
| `tasks[].name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Moco API, this operation is `PUT /projects/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

