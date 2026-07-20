# Atera: Create contact

Creates a contact in Atera.

```
POST https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdOn` | string | no | Contact creation timestamp. |
| `customerId` | number | no | Existing customer ID. |
| `customerName` | string | no | Existing customer name. |
| `departmentId` | number | no | Department ID. |
| `departmentName` | string | no | Department name. |
| `email` | string | yes | Contact email address. |
| `firstname` | string | no | Contact first name. |
| `inIgnoreMode` | boolean | no | Whether the contact is in ignore mode. |
| `isContactPerson` | boolean | no | Whether this is the primary contact person. |
| `jobTitle` | string | no | Job title. |
| `lastname` | string | no | Contact last name. |
| `mobilePhone` | string | no | Mobile phone number. |
| `phone` | string | no | Phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionID` | string |  |

## Native endpoint

Through the native Atera API, this operation is `POST /api/v3/contacts` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

