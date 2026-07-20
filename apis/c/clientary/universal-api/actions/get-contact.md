# Clientary: Get Contact

Retrieves a contact from Clientary by contact ID.

```
GET https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | The Clientary contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "client": {
        "id": 1,
        "name": "Ava Chen",
        "number": "string",
        "status": "string"
      },
      "clientId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "ext": "string",
      "hourlyRate": 1,
      "id": 1,
      "isClientUser": true,
      "miniAvatarUrl": "https://example.com",
      "mobile": "string",
      "name": "Ava Chen",
      "phone": "string",
      "role": 1,
      "thumbAvatarUrl": "https://example.com",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `client.id` | number |  |
| `client.name` | string |  |
| `client.number` | string |  |
| `client.status` | string |  |
| `clientId` | number |  |
| `createdAt` | date |  |
| `email` | string |  |
| `ext` | string |  |
| `hourlyRate` | number |  |
| `id` | number |  |
| `isClientUser` | boolean |  |
| `miniAvatarUrl` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `role` | number |  |
| `thumbAvatarUrl` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Clientary API, this operation is `GET /contacts/:id` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

