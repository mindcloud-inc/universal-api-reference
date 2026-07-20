# Spoki: Update Contact

Updates a contact by ID.

```
PUT https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The contact ID. |
| `phone` | string | yes | The contact phone number. Include the current phone number when updating a contact. |
| `firstName` | string | no | The contact first name. |
| `lastName` | string | no | The contact last name. |
| `email` | string | no | The contact email address. |
| `language` | string | no | The contact language code. |
| `customFields` | object | no | Custom fields keyed by Spoki field code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatLink": "https://example.com",
      "contactfieldSet": [
        {}
      ],
      "contactfieldValues": {},
      "createdDatetime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasInvalidPhone": true,
      "id": 1,
      "isBlocked": true,
      "isRestricted": true,
      "language": "string",
      "lastName": "Chen",
      "listSet": [
        {}
      ],
      "phone": "string",
      "roleSet": [
        {}
      ],
      "status": "string",
      "tagSet": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatLink` | string |  |
| `contactfieldSet` | array<object> |  |
| `contactfieldValues` | object |  |
| `createdDatetime` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `hasInvalidPhone` | boolean |  |
| `id` | number |  |
| `isBlocked` | boolean |  |
| `isRestricted` | boolean |  |
| `language` | string |  |
| `lastName` | string |  |
| `listSet` | array<object> |  |
| `phone` | string |  |
| `roleSet` | array<object> |  |
| `status` | string |  |
| `tagSet` | array<object> |  |

## Native endpoint

Through the native Spoki API, this operation is `PATCH /contacts/{{id}}/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

