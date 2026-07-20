# Trust: Create Contact

Creates a new contact in Trust.

```
POST https://connect.mindcloud.co/v1/universal/trust/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trust/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trust/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Email address of contact. |
| `firstname` | string | no | First name of contact. |
| `imageUrl` | string | no | URL to the contact image. |
| `lastname` | string | no | Last name of contact. |
| `phone` | string | no | Phone number of the contact. |
| `workspaceId` | string | yes | The Trust workspace id (typeId). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "imageUrl": "https://example.com",
      "lastName": "Chen",
      "phone": "string",
      "typeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `created` | date |  |
| `customerId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `imageUrl` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `typeId` | string |  |

## Native endpoint

Through the native Trust API, this operation is `POST /contacts` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

