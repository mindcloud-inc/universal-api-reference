# Moco: Update User



```
PUT https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-user', {
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
| `active` | string | no |  |
| `avatar` | string | no |  |
| `bday` | string | no |  |
| `customProperties` | string | no |  |
| `email` | string | no |  |
| `external` | string | no |  |
| `firstname` | string | no |  |
| `homeAddress` | string | no |  |
| `iban` | string | no |  |
| `id` | number | yes |  |
| `info` | string | no |  |
| `language` | string | no |  |
| `lastname` | string | no |  |
| `mobilePhone` | string | no |  |
| `password` | string | no |  |
| `roleId` | string | no |  |
| `tags` | string | no |  |
| `unitId` | string | no |  |
| `welcomeEmail` | string | no |  |
| `workPhone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avatarUrl": {},
      "birthday": {},
      "createdAt": "string",
      "customProperties": {},
      "email": "ava@example.com",
      "extern": true,
      "firstname": "Ava",
      "homeAddress": "string",
      "iban": {},
      "id": 1,
      "info": "string",
      "lastname": "Chen",
      "mobilePhone": "string",
      "role": {},
      "tags": [
        [
          "string"
        ]
      ],
      "unit": {
        "id": 1,
        "name": "Ava Chen"
      },
      "updatedAt": "string",
      "workPhone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatarUrl` | object |  |
| `birthday` | object |  |
| `createdAt` | string |  |
| `customProperties` | object |  |
| `email` | string |  |
| `extern` | boolean |  |
| `firstname` | string |  |
| `homeAddress` | string |  |
| `iban` | object |  |
| `id` | number |  |
| `info` | string |  |
| `lastname` | string |  |
| `mobilePhone` | string |  |
| `role` | object |  |
| `tags[]` | array<string> |  |
| `unit` | object |  |
| `unit.id` | number |  |
| `unit.name` | string |  |
| `updatedAt` | string |  |
| `workPhone` | string |  |

## Native endpoint

Through the native Moco API, this operation is `PUT /users/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

