# PhoneBurner: Create Contact

Creates a new contact in PhoneBurner.

```
POST https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhoneBurner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/create-contact', {
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
| `email` | string | no | Primary email address for the contact. |
| `first_name` | string | no | First name of the contact. |
| `last_name` | string | no | Last name of the contact. |
| `notes` | string | no | Notes to store on the contact. |
| `phone` | string | no | Primary phone number for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactUserId": "string",
      "dateAdded": "string",
      "emailAddress": "ava@example.com",
      "externalCrmData": [
        {}
      ],
      "firstName": "Ava",
      "importResult": "string",
      "lastName": "Chen",
      "leadId": "string",
      "notes": "string",
      "phone": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactUserId` | string |  |
| `dateAdded` | string |  |
| `emailAddress` | string |  |
| `externalCrmData` | array<object> |  |
| `firstName` | string |  |
| `importResult` | string |  |
| `lastName` | string |  |
| `leadId` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native PhoneBurner API, this operation is `POST rest/1/contacts` (base URL `https://www.phoneburner.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

