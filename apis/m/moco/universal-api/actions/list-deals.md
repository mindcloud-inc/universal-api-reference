# Moco: List Deals



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-deals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-deals?${params}`, {
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
| `closedFrom` | date | no |  |
| `closedTo` | date | no |  |
| `companyId` | number | no |  |
| `customProperties` | object | no |  |
| `ids` | string | no |  |
| `status` | string | no |  |
| `tags` | string | no |  |
| `updatedAfter` | date | no |  |

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
      "company": {},
      "createdAt": "string",
      "currency": "string",
      "customer": {},
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
| `createdAt` | string |  |
| `currency` | string |  |
| `customer` | object |  |
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

Through the native Moco API, this operation is `GET /deals` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

