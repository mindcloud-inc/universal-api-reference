# Peach: Update Contact

Updates an existing contact in Peach.

```
PUT https://connect.mindcloud.co/v1/universal/peach/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/peach/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peach/latest/actions/update-contact', {
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
| `contactId` | string | yes | The contact ID to update. |
| `firstName` | string | no | Contact's first name. |
| `lastName` | string | no | Contact's last name. |
| `email` | string | no | Contact's email address. |
| `phone` | string | no | Contact's phone number. |
| `address` | string | no | Contact address. |
| `city` | string | no | Contact city. |
| `street` | string | no | Contact street. |
| `streetNumber` | string | no | Contact street number. |
| `aptNumber` | string | no | Contact apartment number. |
| `zipCode` | string | no | Contact zip code. |
| `groups[]` | array<string> | no | Group names to add to the contact. |
| `removeGroups[]` | array<string> | no | Group names to remove from the contact. |
| `customProperties` | object | no | Custom properties for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "contactBody": {
          "address": "string",
          "aptNumber": "string",
          "city": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "street": "string",
          "streetNumber": "string",
          "telephone": "string",
          "zipCode": "string"
        }
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
| `contact` | object |  |
| `contact.contactBody` | object |  |
| `contact.contactBody.address` | string |  |
| `contact.contactBody.aptNumber` | string |  |
| `contact.contactBody.city` | string |  |
| `contact.contactBody.email` | string |  |
| `contact.contactBody.firstName` | string |  |
| `contact.contactBody.lastName` | string |  |
| `contact.contactBody.street` | string |  |
| `contact.contactBody.streetNumber` | string |  |
| `contact.contactBody.telephone` | string |  |
| `contact.contactBody.zipCode` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Peach API, this operation is `PUT /updateContact/:contactId` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

