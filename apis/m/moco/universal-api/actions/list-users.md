# Moco: List Users



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-users?${params}`, {
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
| `customProperties` | object | no |  |
| `email` | string | no |  |
| `ids` | string | no |  |
| `includeArchived` | boolean | no |  |
| `tags` | string | no |  |
| `updatedAfter` | date | no |  |

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
      "role": {
        "id": 1,
        "name": "Ava Chen"
      },
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
| `role.id` | number |  |
| `role.name` | string |  |
| `tags[]` | array<string> |  |
| `unit` | object |  |
| `unit.id` | number |  |
| `unit.name` | string |  |
| `updatedAt` | string |  |
| `workPhone` | string |  |

## Native endpoint

Through the native Moco API, this operation is `GET /users` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

