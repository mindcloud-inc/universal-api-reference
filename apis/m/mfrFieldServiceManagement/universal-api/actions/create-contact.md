# mfr Field Service Management: Create Contact

Creates a contact in mfr Field Service Management.

```
POST https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen"
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
| `email` | string | no | Contact email address. |
| `companyId` | string | no | Company ID linked to the contact. |
| `externalId` | string | no | External identifier for the contact. |
| `mobilePhone` | string | no | Contact mobile phone number. |
| `telephone` | string | no | Contact telephone number. |
| `isUser` | boolean | no | Whether the contact is a user. |
| `gender` | string | no | Contact gender. |
| `fax` | string | no | Contact fax number. |
| `note` | string | no | Contact note. |
| `jobTitle` | string | no | Contact job title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "customValues": [
        {}
      ],
      "dateModified": "string",
      "email": "ava@example.com",
      "externalId": "string",
      "fax": "string",
      "firstName": "Ava",
      "gender": "string",
      "groupId": "string",
      "id": 1,
      "isUser": true,
      "jobTitle": "string",
      "lastName": "Chen",
      "mobilePhone": "string",
      "note": "string",
      "telephone": "string",
      "userId": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `customValues` | array<object> |  |
| `dateModified` | string |  |
| `email` | string |  |
| `externalId` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `groupId` | string |  |
| `id` | number |  |
| `isUser` | boolean |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `mobilePhone` | string |  |
| `note` | string |  |
| `telephone` | string |  |
| `userId` | string |  |
| `version` | number |  |

## Native endpoint

Through the native mfr Field Service Management API, this operation is `POST Contacts` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

