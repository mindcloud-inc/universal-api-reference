# Blooio Messaging: Get Contact

Retrieves a contact from Blooio Messaging.

```
GET https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blooio Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-contact?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-contact?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Contact identifier. Use an E.164 phone number or email address. |

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

Through the native Blooio Messaging API, this operation is `GET /contacts/{identifier}` (base URL `https://backend.blooio.com/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

