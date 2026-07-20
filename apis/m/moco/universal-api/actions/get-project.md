# Moco: Get Project



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-project?${params}`, {
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
| `id` | number | yes | Project ID |

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
      "finishDate": "string",
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
| `finishDate` | string |  |
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

Through the native Moco API, this operation is `GET /projects/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

