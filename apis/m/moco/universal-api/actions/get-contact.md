# Moco: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | Contact ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": {},
      "birthday": {},
      "company": {},
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

Through the native Moco API, this operation is `GET /contacts/people/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

