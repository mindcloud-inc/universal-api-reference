# ProProfs Project: Create Contact

Creates a new contact in ProProfs Project.

```
POST https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | no | Associate the contact with a client. |
| `contactName` | string | yes | The contact name. |
| `email` | string | no | The contact email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "companyName": "Ava Chen",
      "contactId": "string",
      "contactName": "Ava Chen",
      "dateCreated": "string",
      "dateModified": "string",
      "email": "ava@example.com",
      "fax": "string",
      "mobile": "string",
      "role": "string",
      "tel": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string |  |
| `companyName` | string |  |
| `contactId` | string |  |
| `contactName` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `email` | string |  |
| `fax` | string |  |
| `mobile` | string |  |
| `role` | string |  |
| `tel` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `POST /contacts` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

