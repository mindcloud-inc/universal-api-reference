# Yousign: Update Contact

Updates an existing contact in Yousign.

```
PUT https://connect.mindcloud.co/v1/universal/yousign/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yousign/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The Yousign contact ID. |
| `firstName` | string | no | Updated contact first name. |
| `lastName` | string | no | Updated contact last name. |
| `email` | string | no | Updated contact email address. |
| `locale` | string | no | Updated contact locale. |
| `phoneNumber` | string | no | Updated contact phone number in E.164 format. |
| `companyName` | string | no | Updated contact company name. |
| `jobTitle` | string | no | Updated contact job title. |
| `workspaceId` | string | no | Updated contact workspace ID. |
| `addressLine1` | string | no | Updated contact address line 1. |
| `addressLine2` | string | no | Updated contact address line 2. |
| `addressCity` | string | no | Updated contact address city. |
| `addressPostalCode` | string | no | Updated contact address postal code. |
| `addressCountry` | string | no | Updated contact address country. |

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

Through the native Yousign API, this operation is `PATCH /contacts/:contactId` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

