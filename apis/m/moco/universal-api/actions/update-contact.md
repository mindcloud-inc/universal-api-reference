# Moco: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-contact', {
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
| `birthday` | string | no |  |
| `companyId` | string | no |  |
| `firstname` | string | no |  |
| `gender` | string | no |  |
| `homeAddress` | string | no |  |
| `homeEmail` | string | no |  |
| `id` | number | yes |  |
| `info` | string | no |  |
| `jobPosition` | string | no |  |
| `lastname` | string | no |  |
| `mobilePhone` | string | no |  |
| `tags` | string | no |  |
| `title` | string | no |  |
| `userId` | string | no |  |
| `workAddress` | string | no |  |
| `workEmail` | string | no |  |
| `workFax` | string | no |  |
| `workPhone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": {},
      "birthday": {},
      "company": {
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "createdAt": "string",
      "customProperties": {},
      "firstname": "Ava",
      "gender": "string",
      "homeAddress": "string",
      "homeEmail": "ava@example.com",
      "id": 1,
      "info": "string",
      "jobPosition": "string",
      "lastname": "Chen",
      "mobilePhone": "string",
      "salutation": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "title": "string",
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      },
      "workAddress": "string",
      "workEmail": "ava@example.com",
      "workFax": "string",
      "workPhone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | object |  |
| `birthday` | object |  |
| `company` | object |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `company.type` | string |  |
| `createdAt` | string |  |
| `customProperties` | object |  |
| `firstname` | string |  |
| `gender` | string |  |
| `homeAddress` | string |  |
| `homeEmail` | string |  |
| `id` | number |  |
| `info` | string |  |
| `jobPosition` | string |  |
| `lastname` | string |  |
| `mobilePhone` | string |  |
| `salutation` | string |  |
| `tags[]` | array<string> |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |
| `workAddress` | string |  |
| `workEmail` | string |  |
| `workFax` | string |  |
| `workPhone` | string |  |

## Native endpoint

Through the native Moco API, this operation is `PUT /contacts/people/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

