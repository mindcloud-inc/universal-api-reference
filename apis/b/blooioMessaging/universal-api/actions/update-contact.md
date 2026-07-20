# Blooio Messaging: Update Contact

Updates an existing contact in Blooio Messaging.

```
PUT https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blooio Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/update-contact', {
  method: 'PUT',
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
      "contact_id": "string",
      "created_at": 1,
      "id": "string",
      "identifier": "string",
      "last_message_time": 1,
      "name": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_id` | string |  |
| `created_at` | number |  |
| `id` | string |  |
| `identifier` | string |  |
| `last_message_time` | number |  |
| `name` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Blooio Messaging API, this operation is `PATCH /contacts/{identifier}` (base URL `https://backend.blooio.com/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

