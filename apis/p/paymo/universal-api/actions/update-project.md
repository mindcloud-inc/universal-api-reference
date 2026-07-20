# Paymo: Update Project

Updates an existing project in Paymo.

```
PUT https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The Paymo project id. |
| `name` | string | no | Updated project name. |
| `description` | string | no | Updated project description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "billable": true,
      "billingType": "string",
      "clientId": 1,
      "clientName": "Ava Chen",
      "code": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "flatBilling": true,
      "id": 1,
      "managers": [
        1
      ],
      "name": "Ava Chen",
      "taskCodeIncrement": 1,
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "users": [
        1
      ],
      "workflowId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billable` | boolean |  |
| `billingType` | string |  |
| `clientId` | number |  |
| `clientName` | string |  |
| `code` | string |  |
| `createdOn` | date |  |
| `description` | string |  |
| `flatBilling` | boolean |  |
| `id` | number |  |
| `managers` | array<number> |  |
| `name` | string |  |
| `taskCodeIncrement` | number |  |
| `updatedOn` | date |  |
| `users` | array<number> |  |
| `workflowId` | number |  |

## Native endpoint

Through the native Paymo API, this operation is `PUT projects/:projectId` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

