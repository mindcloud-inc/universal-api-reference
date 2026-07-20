# SalesRender: Update User

Updates an existing user in SalesRender.

```
PUT https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation UpdateUser($input: UpdateUserInput!) {\n  userMutation {\n    updateUser(input: $input) {\n      id\n      email\n      registeredAt\n    }\n  }\n}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation UpdateUser($input: UpdateUserInput!) {\n  userMutation {\n    updateUser(input: $input) {\n      id\n      email\n      registeredAt\n    }\n  }\n}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | GraphQL variables object. Set `input` to a valid UpdateUserInput payload. Default: `{"input":{}}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation to execute. Default: `mutation UpdateUser($input: UpdateUserInput!) {\n  userMutation {\n    updateUser(input: $input) {\n      id\n      email\n      registeredAt\n    }\n  }\n}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "userMutation": {
          "updateUser": {
            "email": "ava@example.com",
            "id": "string",
            "registeredAt": "2026-05-07T12:00:00.000Z"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.userMutation.updateUser.email` | string |  |
| `data.userMutation.updateUser.id` | string |  |
| `data.userMutation.updateUser.registeredAt` | date |  |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

