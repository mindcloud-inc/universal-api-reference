# FreshBooks: Update Project

Updates an existing project in FreshBooks for a business.

```
PUT https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes | FreshBooks business ID. |
| `projectId` | string | yes | FreshBooks project ID. |
| `project.title` | string | no | Project title. |
| `project.client_id` | number | no | FreshBooks client ID. |
| `project.project_type` | string | no | FreshBooks project type. |
| `project.fixed_price` | string | no | Fixed-price amount. |
| `project.rate` | string | no | Hourly rate amount. |
| `project.description` | string | no | Project description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "billedAmount": "string",
      "billedStatus": "string",
      "billingMethod": "string",
      "budget": 1,
      "clientId": 1,
      "complete": true,
      "createdAt": "string",
      "description": "string",
      "dueDate": "string",
      "expenseMarkup": "string",
      "fixedPrice": "string",
      "group": {},
      "groupId": 1,
      "id": 1,
      "internal": true,
      "loggedDuration": 1,
      "projectManagerId": 1,
      "projectType": "string",
      "rate": "string",
      "retainerId": 1,
      "sample": true,
      "serviceEstimateType": "string",
      "services": [
        {}
      ],
      "title": "string",
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
| `billedAmount` | string |  |
| `billedStatus` | string |  |
| `billingMethod` | string |  |
| `budget` | number |  |
| `clientId` | number |  |
| `complete` | boolean |  |
| `createdAt` | string |  |
| `description` | string |  |
| `dueDate` | string |  |
| `expenseMarkup` | string |  |
| `fixedPrice` | string |  |
| `group` | object |  |
| `groupId` | number |  |
| `id` | number |  |
| `internal` | boolean |  |
| `loggedDuration` | number |  |
| `projectManagerId` | number |  |
| `projectType` | string |  |
| `rate` | string |  |
| `retainerId` | number |  |
| `sample` | boolean |  |
| `serviceEstimateType` | string |  |
| `services` | array<object> |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native FreshBooks API, this operation is `PUT /projects/business/:businessId/project/:projectId` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

