# Constant Contact: Create Contact

Creates a contact in Constant Contact.

```
POST https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "person@example.com",
  "permissionToSend": "Select permission level",
  "createSource": "Account"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "person@example.com",
    "permissionToSend": "Select permission level",
    "createSource": "Account"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Primary email address for the contact (must be unique in Constant Contact). Example: `person@example.com`. |
| `permissionToSend` | string | yes | Permission level for sending email to this contact. One of: `0`, `1`, `2`, `3`, `4`, `5`. Example: `Select permission level`. |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `createSource` | string | yes | Who created the contact (required for compliance). One of: `0`, `1`. Default: `Account`. Example: `Account`. |
| `listMemberships[]` | array<string> | no | Optional. Array of list IDs. Do not pass objects; each item must be a list_id string. One of: `0`. Accepts multiple values as an array. Example: `Optional: choose list(s)`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createSource": "string",
      "emailAddress": {},
      "firstName": "Ava",
      "lastName": "Chen",
      "listMemberships": [
        "string"
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
| `contactId` | string | Unique contact identifier. |
| `createdAt` | date | Created timestamp (ISO-8601). |
| `createSource` | string | Source that created the contact. |
| `emailAddress` | object | Email address subresource for the contact. |
| `firstName` | string | Contact first name. |
| `lastName` | string | Contact last name. |
| `listMemberships` | array<string> | List IDs the contact belongs to when provided. |
| `updatedAt` | date | Last updated timestamp (ISO-8601). |

## Native endpoint

Through the native Constant Contact API, this operation is `POST /contacts` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

