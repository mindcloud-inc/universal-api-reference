# ClickMeeting: Register Conference Participant

Creates a conference participant registration in ClickMeeting.

```
POST https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/register-conference-participant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/register-conference-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room_id": 1,
  "first_name": "Ava",
  "last_name": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/register-conference-participant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room_id": 1,
    "first_name": "Ava",
    "last_name": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room_id` | number | yes | Conference room identifier. |
| `first_name` | string | yes | Participant first name. |
| `last_name` | string | yes | Participant last name. |
| `email` | string | yes | Participant email address. |
| `confirmation_email_enabled` | boolean | no | Enable ClickMeeting confirmation email delivery. |
| `confirmation_email_lang` | string | no | Confirmation email language token. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Registration result status. |
| `url` | string | Registered participant join URL. |

## Native endpoint

Through the native ClickMeeting API, this operation is `POST conferences/{{room_id}}/registration` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-conference-participant.md) for the provider-specific parameters and requirements.

