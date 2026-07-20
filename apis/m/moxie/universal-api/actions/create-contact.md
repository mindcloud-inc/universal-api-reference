# Moxie: Create Contact

Creates a new contact in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "first": "string",
  "last": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "first": "string",
    "last": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `first` | string | yes | Contact first name. |
| `last` | string | yes | Contact last name. |
| `email` | string | no | Contact email address. |
| `phone` | string | no | Contact phone number. |
| `clientName` | string | no | Existing client name to attach the contact to. |
| `defaultContact` | boolean | no | Whether this should be the default client contact. |
| `portalAccess` | boolean | no | Whether the contact should have portal access. |
| `invoiceContact` | boolean | no | Whether the contact should receive invoices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "clientId": "string",
      "clientPortalUserId": 1,
      "defaultContact": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "invoiceContact": true,
      "lastName": "Chen",
      "phone": "string",
      "portalAccess": true,
      "role": "string",
      "sampleData": true,
      "searchObject": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `clientId` | string |  |
| `clientPortalUserId` | number |  |
| `defaultContact` | boolean |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `invoiceContact` | boolean |  |
| `lastName` | string |  |
| `phone` | string |  |
| `portalAccess` | boolean |  |
| `role` | string |  |
| `sampleData` | boolean |  |
| `searchObject` | object |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/contacts/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

