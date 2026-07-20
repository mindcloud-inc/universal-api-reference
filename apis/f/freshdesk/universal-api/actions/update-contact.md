# Freshdesk: Update Contact

Updates an existing contact in Freshdesk.

```
PUT https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | list<number> | yes | Freshdesk contact ID. |
| `name` | string | no | Name of the contact |
| `email` | string | no | Primary email address of the contact |
| `phone` | string | no | Telephone number of the contact |
| `mobile` | string | no | Mobile number of the contact |
| `twitterId` | string | no | Twitter handle of the contact |
| `socialHandler[]` | array<object> | no | Social handles for the contact |
| `uniqueExternalId` | string | no | External ID of the contact |
| `otherEmails[]` | array<string> | no | Additional emails associated with the contact |
| `companyId` | list<number> | no | Primary company ID for the contact |
| `viewAllTickets` | boolean | no | Whether contact can view all company tickets |
| `otherCompanies[]` | array<object> | no | Additional companies associated with the contact |
| `address` | string | no | Address of the contact |
| `avatar` | file | no | Avatar image of the contact |
| `customFields` | object | no | Key-value pairs for custom contact fields |
| `description` | string | no | Short description of the contact |
| `jobTitle` | string | no | Job title of the contact |
| `language` | string | no | Language of the contact |
| `tags[]` | array<string> | no | Tags associated with the contact |
| `timeZone` | string | no | Time zone of the contact |
| `lookupParameter` | string | no | Lookup field value for custom object linkage |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "companyId": 1,
      "contactType": "string",
      "createdAt": "string",
      "deleted": true,
      "email": "ava@example.com",
      "id": 1,
      "mobile": "string",
      "name": "Ava Chen",
      "phone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `companyId` | number |  |
| `contactType` | string |  |
| `createdAt` | string |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `mobile` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshdesk API, this operation is `PUT /contacts/:id` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

