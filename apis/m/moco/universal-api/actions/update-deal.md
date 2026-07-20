# Moco: Update Deal



```
PUT https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-deal', {
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
| `closedOn` | string | no |  |
| `companyId` | string | no |  |
| `currency` | string | no |  |
| `dealCategoryId` | string | no |  |
| `id` | number | yes |  |
| `info` | string | no |  |
| `money` | string | no |  |
| `name` | string | no |  |
| `personId` | string | no |  |
| `reminderDate` | string | no |  |
| `servicePeriodFrom` | string | no |  |
| `servicePeriodTo` | string | no |  |
| `status` | string | no |  |
| `tags` | string | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {
        "id": 1,
        "name": "Ava Chen",
        "probability": 1
      },
      "closedOn": {},
      "company": {
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "createdAt": "string",
      "currency": "string",
      "customer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "customProperties": {},
      "id": 1,
      "inboxEmailAddress": "ava@example.com",
      "info": "string",
      "money": 1,
      "name": "Ava Chen",
      "person": {},
      "reminderDate": "string",
      "servicePeriodFrom": {},
      "servicePeriodTo": {},
      "status": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object |  |
| `category.id` | number |  |
| `category.name` | string |  |
| `category.probability` | number |  |
| `closedOn` | object |  |
| `company` | object |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `company.type` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customer` | object |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customProperties` | object |  |
| `id` | number |  |
| `inboxEmailAddress` | string |  |
| `info` | string |  |
| `money` | number |  |
| `name` | string |  |
| `person` | object |  |
| `reminderDate` | string |  |
| `servicePeriodFrom` | object |  |
| `servicePeriodTo` | object |  |
| `status` | string |  |
| `tags[]` | array<string> |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |

## Native endpoint

Through the native Moco API, this operation is `PUT /deals/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

