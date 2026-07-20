# Onfleet: Create Recipient

Creates a new recipient in Onfleet.

```
POST https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The recipient's complete name. |
| `phone` | string | yes | The recipient's phone number. |
| `notes` | string | no | Optional notes for this recipient. |
| `skipSMSNotifications` | boolean | no | Whether this recipient should skip SMS notifications. |
| `skipPhoneNumberValidation` | boolean | no | Whether to skip phone number validation for this recipient. |
| `useLongCodeForText` | boolean | no | Whether to use a toll-free long code number for SMS communication. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "skipSMSNotifications": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `skipSMSNotifications` | boolean |  |

## Native endpoint

Through the native Onfleet API, this operation is `POST /recipients` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient.md) for the provider-specific parameters and requirements.

