# Clientary: Create Contact

Creates a new contact for a client in Clientary.

```
POST https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client_id": "string",
  "clientUser.email": "ava@example.com",
  "clientUser.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client_id": "string",
    "clientUser.email": "ava@example.com",
    "clientUser.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client_id` | string | yes | The parent client ID. |
| `clientUser.email` | string | yes | The contact email address. |
| `clientUser.name` | string | yes | The contact name. |

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

Through the native Clientary API, this operation is `POST /clients/:client_id/contacts` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

