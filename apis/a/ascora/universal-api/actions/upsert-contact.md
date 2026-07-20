# Ascora: Upsert Contact

Creates or updates a contact in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/upsert-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/upsert-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/upsert-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | no |  |
| `customerId` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `emailAddress` | string | no |  |
| `phoneNumber` | string | no |  |
| `mobileNumber` | string | no |  |
| `faxNumber` | string | no |  |
| `defaultContact` | boolean | no |  |
| `contactRole` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "contactId": "string",
        "contactRole": "string",
        "customerId": "string",
        "defaultContact": true,
        "emailAddress": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobileNumber": "string",
        "phoneNumber": "string"
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.contactId` | string | ID of the contact. |
| `contact.contactRole` | string | Contact role name. |
| `contact.customerId` | string | ID of the parent customer. |
| `contact.defaultContact` | boolean | Whether this is the default contact. |
| `contact.emailAddress` | string | Contact email address. |
| `contact.firstName` | string | Contact first name. |
| `contact.lastName` | string | Contact last name. |
| `contact.mobileNumber` | string | Contact mobile number. |
| `contact.phoneNumber` | string | Contact phone number. |
| `message` | string | Ascora status message. |
| `success` | boolean | Whether Ascora created or updated the contact. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Customers/Contact` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-contact.md) for the provider-specific parameters and requirements.

