# Yousign: Create Contact

Creates a new contact in Yousign.

```
POST https://connect.mindcloud.co/v1/universal/yousign/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com",
  "locale": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yousign/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com",
    "locale": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Contact first name. |
| `lastName` | string | yes | Contact last name. |
| `email` | string | yes | Contact email address. |
| `locale` | string | yes | Contact locale. |
| `phoneNumber` | string | no | Contact phone number in E.164 format. |
| `companyName` | string | no | Company name for the contact. |
| `jobTitle` | string | no | Job title for the contact. |
| `workspaceId` | string | no | Workspace ID to associate with the contact. |
| `addressLine1` | string | no | Primary street address line. |
| `addressLine2` | string | no | Secondary street address line. |
| `addressCity` | string | no | City for the contact address. |
| `addressPostalCode` | string | no | Postal code for the contact address. |
| `addressCountry` | string | no | Country for the contact address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressCity": "string",
      "addressCountry": "string",
      "addressLine1": "string",
      "addressLine2": "string",
      "addressPostalCode": "string",
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "locale": "string",
      "phoneNumber": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressCity` | string | Contact address city. |
| `addressCountry` | string | Contact address country. |
| `addressLine1` | string | Contact address line 1. |
| `addressLine2` | string | Contact address line 2. |
| `addressPostalCode` | string | Contact address postal code. |
| `companyName` | string | Contact company name. |
| `createdAt` | date | Contact creation timestamp. |
| `email` | string | Contact email address. |
| `firstName` | string | Contact first name. |
| `id` | string | Contact ID. |
| `jobTitle` | string | Contact job title. |
| `lastName` | string | Contact last name. |
| `locale` | string | Contact locale. |
| `phoneNumber` | string | Contact phone number in E.164 format. |
| `workspaceId` | string | Workspace ID associated with the contact. |

## Native endpoint

Through the native Yousign API, this operation is `POST /contacts` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

