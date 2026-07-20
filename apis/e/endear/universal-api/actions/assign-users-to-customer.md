# Endear: Assign Users To Customer



```
PUT https://connect.mindcloud.co/v1/universal/endear/latest/actions/assign-users-to-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Endear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/endear/latest/actions/assign-users-to-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string",
  "variables.assigneeIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/endear/latest/actions/assign-users-to-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string",
    "variables.assigneeIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.assignerId` | string | no | Assigner Id for the Endear GraphQL operation. |
| `variables.id` | string | yes | Id for the Endear GraphQL operation. |
| `variables.assigneeIds[]` | array<string> | yes | Assignee Ids for the Endear GraphQL operation. |
| `variables.skipIfCustomerAlreadyAssigned` | boolean | no | Skip If Customer Already Assigned for the Endear GraphQL operation. |
| `variables.notifyAssignees` | boolean | no | Notify Assignees for the Endear GraphQL operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Endear API, this operation is `POST /graphql` (base URL `https://api.endearhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-users-to-customer.md) for the provider-specific parameters and requirements.

