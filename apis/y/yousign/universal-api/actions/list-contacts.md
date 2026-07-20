# Yousign: List Contacts

Retrieves contacts from Yousign.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-contacts?${params}`, {
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
| `after` | string | no | Return contacts after this pagination cursor. |
| `limit` | number | no | Maximum number of contacts to return. |

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

Through the native Yousign API, this operation is `GET /contacts` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

