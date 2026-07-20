# updown.io: Create Recipient

Creates a new alert recipient in updown.io.

```
POST https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "email",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "email",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Optional label for recipient types that support it. |
| `selected` | boolean | no | Whether the new recipient is selected on all existing checks. |
| `type` | list | yes | Recipient type: email, sms, webhook, slack_compatible, or msteams. One of: `email`, `msteams`, `slack_compatible`, `sms`, `webhook`. |
| `value` | string | yes | The recipient value, such as an email address, phone number, or URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Recipient identifier. |
| `name` | string | Recipient display name. |
| `type` | string | Recipient channel type. |
| `value` | string | Recipient destination value. |

## Native endpoint

Through the native updown.io API, this operation is `POST /recipients` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient.md) for the provider-specific parameters and requirements.

