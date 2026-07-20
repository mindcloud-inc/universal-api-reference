# SendMe: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `birthDate` | date | no | Birth date. |
| `countryCode` | string | no | Country code. |
| `customValues` | object | no | Custom field values. |
| `email` | string | no | Contact email address. |
| `id` | string | yes | Unique contact ID. |
| `lastName` | string | no | Contact last name. |
| `phone` | string | no | Phone number. |
| `status` | string | no | Contact status. |
| `tagIds` | list<string> | no | Tag IDs to associate. |

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

Through the native SendMe API, this operation is `PATCH /api/contacts/:id` (base URL `https://app.sendme123.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

