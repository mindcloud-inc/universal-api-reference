# HappyFox: Create Contact

Creates a new contact in HappyFox.

```
POST https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Contact name. |
| `email` | string | yes | Contact email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactGroups": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "id": 1,
      "isLoginEnabled": true,
      "name": "Ava Chen",
      "pendingTicketsCount": 1,
      "phones": [
        {}
      ],
      "primaryPhone": "string",
      "ticketsCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactGroups` | array<object> | Contact groups this contact belongs to. |
| `createdAt` | date | Contact creation timestamp. |
| `customFields` | array<object> | Custom field values for the contact. |
| `email` | string | Primary contact email address. |
| `id` | number | Internal HappyFox contact ID. |
| `isLoginEnabled` | boolean | Whether the contact can log in to the portal. |
| `name` | string | Contact display name. |
| `pendingTicketsCount` | number | Pending ticket count for the contact. |
| `phones` | array<object> | Additional phone records. |
| `primaryPhone` | string | Primary phone number, when present. |
| `ticketsCount` | number | Total tickets associated with the contact. |
| `updatedAt` | date | Contact last updated timestamp. |

## Native endpoint

Through the native HappyFox API, this operation is `POST /users/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

