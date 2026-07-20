# Documo: Update Contact

Updates an existing contact in Documo.

```
PUT https://connect.mindcloud.co/v1/universal/documo/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documo/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/update-contact', {
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
| `contactId` | string | yes | String \| Required \| Contact UUID |
| `name` | string | no | String \| Contact name |
| `email` | string | no | String \| Contact email |
| `faxNumber` | string | no | String \| Fax number in E164 or number format with country code included |
| `phoneNumber` | string | no | String \| Phone number in E164 or number format with country code included |
| `organizationId` | string | no | String \| Assign contact to existing organization contact |
| `isPublic` | boolean | no | Boolean \| Show contact for all users in the account |
| `isOrganization` | boolean | no | Boolean \| Create an organization contact when true |
| `publicEditable` | boolean | no | Boolean \| Allow all account users to edit the contact when true |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "faxNumber": "string",
      "isOrganization": true,
      "isPublic": true,
      "lastName": "Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "phoneNumber": "string",
      "publicEditable": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `faxNumber` | string |  |
| `isOrganization` | boolean |  |
| `isPublic` | boolean |  |
| `lastName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `phoneNumber` | string |  |
| `publicEditable` | boolean |  |
| `updatedAt` | date |  |
| `userId` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `PATCH /v1/contacts/:contactId` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

