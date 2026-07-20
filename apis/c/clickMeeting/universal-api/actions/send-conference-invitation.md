# ClickMeeting: Send Conference Invitation

Sends a conference invitation email from ClickMeeting.

```
POST https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/send-conference-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/send-conference-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room_id": 1,
  "lang": "en",
  "attendee_emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/send-conference-invitation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room_id": 1,
    "lang": "en",
    "attendee_emails": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room_id` | number | yes | Conference room identifier. |
| `lang` | string | yes | Invitation language token from ClickMeeting. Default: `en`. |
| `attendee_emails` | string | yes | One or more attendee email addresses. Accepts multiple values as an array. |
| `template` | list | no | Invitation template style. One of: `advanced`, `basic`. |
| `role` | list | no | Invitation recipient role. One of: `listener`, `presenter`. Default: `listener`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Invitation result status. |

## Native endpoint

Through the native ClickMeeting API, this operation is `POST conferences/{{room_id}}/invitation/email/{{lang}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-conference-invitation.md) for the provider-specific parameters and requirements.

