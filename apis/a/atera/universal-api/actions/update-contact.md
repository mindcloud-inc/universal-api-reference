# Atera: Update contact

Updates an existing contact in Atera.

```
PUT https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | boolean | no | Whether the contact is archived. |
| `contactId` | number | yes | System contact ID. |
| `customerId` | number | no | Customer ID. |
| `customerName` | string | no | Customer name. |
| `departmentId` | number | no | Department ID. |
| `departmentName` | string | no | Department name. |
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

Through the native Atera API, this operation is `PUT /api/v3/contacts/:contactId` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

