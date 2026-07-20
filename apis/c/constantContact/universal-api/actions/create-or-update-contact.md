# Constant Contact: Create or Update Contact

Creates or updates a contact in Constant Contact.

```
POST https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-or-update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listMemberships[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-or-update-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listMemberships[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | no | Email address used to create or update the contact. |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `phoneNumber` | string | no | SMS-capable phone number for signup flows. |
| `listMemberships[]` | array<string> | yes | List memberships required by sign-up form endpoint (array of list IDs). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "contactId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `contactId` | string |  |

## Native endpoint

Through the native Constant Contact API, this operation is `POST /contacts/sign_up_form` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-contact.md) for the provider-specific parameters and requirements.

