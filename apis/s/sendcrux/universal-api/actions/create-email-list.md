# Sendcrux: Create Email List

Creates a new email list in Sendcrux.

```
POST https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/create-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/create-email-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "default_subject": "string",
  "from_email": "ava@example.com",
  "from_name": "Ava Chen",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/create-email-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "default_subject": "string",
    "from_email": "ava@example.com",
    "from_name": "Ava Chen",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_address_1` | string | no | The primary street address for the list contact profile. |
| `contact_city` | string | no | The city for the list contact profile. |
| `contact_company` | string | no | The company name for the list contact profile. |
| `contact_country_id` | string | no | The numeric country identifier for the list contact profile. |
| `contact_email` | string | no | The contact email address for the list profile. |
| `contact_state` | string | no | The state or region for the list contact profile. |
| `default_subject` | string | yes | The default subject line for campaigns that use this list. |
| `from_email` | string | yes | The sender email address for the list. |
| `from_name` | string | yes | The sender display name for the list. |
| `name` | string | yes | The display name of the list. |
| `send_welcome_email` | string | no | Set to 1 to send the Sendcrux welcome email to new subscribers. |
| `subscribe_confirmation` | string | no | Set to 1 to require confirmation when people subscribe. |
| `unsubscribe_notification` | string | no | Set to 1 to notify the list owner when someone unsubscribes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "list_uid": "string",
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list_uid` | string |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Sendcrux API, this operation is `POST /api/v1/lists` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-list.md) for the provider-specific parameters and requirements.

