# Blooio Messaging: Create Contact

Creates a new contact in Blooio Messaging.

```
POST https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blooio Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no |  |
| `identifier` | string | yes | Contact identifier. Use an E.164 phone number or email address. |
| `lastName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "createdAt": 1,
      "id": "string",
      "identifier": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `createdAt` | number |  |
| `id` | string |  |
| `identifier` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Blooio Messaging API, this operation is `POST /contacts` (base URL `https://backend.blooio.com/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

