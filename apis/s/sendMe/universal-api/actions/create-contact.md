# SendMe: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `birthDate` | date | no | Birth date value. |
| `countryCode` | string | no | Country code (for example 57). |
| `customValues` | object | no | Custom field values. |
| `email` | string | no | Contact email address. |
| `lastName` | string | no | Contact last name. |
| `name` | string | yes | Contact name. |
| `phone` | string | yes | Phone number without country prefix. |
| `status` | string | no | Contact status (ACTIVE, INACTIVE, BLOCKED). |
| `tagIds` | list<string> | no | Associated tag IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthDate": "2026-05-07T12:00:00.000Z",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customValues": [
        {}
      ],
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "lastName": "Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "origin": "string",
      "phone": "string",
      "status": "string",
      "tags": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthDate` | date |  |
| `countryCode` | string |  |
| `createdAt` | date |  |
| `customValues` | array<object> |  |
| `deletedAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `origin` | string |  |
| `phone` | string |  |
| `status` | string |  |
| `tags` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native SendMe API, this operation is `POST /api/contacts` (base URL `https://app.sendme123.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

