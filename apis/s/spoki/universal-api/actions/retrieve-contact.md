# Spoki: Retrieve Contact

Retrieves a contact by ID.

```
GET https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-contact?${params}`, {
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
| `id` | number | yes | The contact ID. |

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

Through the native Spoki API, this operation is `GET /contacts/{{id}}/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

