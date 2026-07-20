# Moco: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-contacts?${params}`, {
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
| `ids` | string | no |  |
| `phone` | string | no |  |
| `tags` | string | no |  |
| `term` | string | no |  |
| `updatedAfter` | date | no |  |

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

Through the native Moco API, this operation is `GET /contacts/people` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

