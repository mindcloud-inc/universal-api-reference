# SalesRender: Create User

Creates a new user in SalesRender.

```
POST https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation CreateUser($input: AddUserInput!) {\n  userMutation {\n    addUser(input: $input) {\n      id\n      email\n      registeredAt\n    }\n  }\n}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation CreateUser($input: AddUserInput!) {\n  userMutation {\n    addUser(input: $input) {\n      id\n      email\n      registeredAt\n    }\n  }\n}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | GraphQL variables object. Set `input` to a valid AddUserInput payload. Default: `{"input":{}}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation to execute. Default: `mutation CreateUser($input: AddUserInput!) {\n  userMutation {\n    addUser(input: $input) {\n      id\n      email\n      registeredAt\n    }\n  }\n}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "userMutation": {
          "addUser": {
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
| `data.userMutation.addUser.email` | string |  |
| `data.userMutation.addUser.id` | string |  |
| `data.userMutation.addUser.registeredAt` | date |  |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

