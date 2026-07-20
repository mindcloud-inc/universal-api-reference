# SmartSurvey: Send Survey Invitation

Sends a SmartSurvey invitation to one recipient.

```
POST https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/send-survey-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/send-survey-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "invitationId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/send-survey-invitation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "invitationId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | The survey id whose Invitation you are querying |
| `invitationId` | number | yes | The invitation id that you are querying |
| `name` | string | yes | The name of the contact to send the invitation to |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | The email address of the target for this invitation (if an email invitation) |
| `mobile` | string | no | The mobile/cell number for the target for this invitation (if an SMS invitation) |
| `customColumns[]` | array<object> | no | Custom column values for this recipient, if needed |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed_contacts": {
        "contact": "string",
        "error_message": "string",
        "mail_user_id": 1,
        "name": "Ava Chen",
        "status_code": "string"
      },
      "message": "string",
      "validation_errors": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed_contacts` | array<object> |  |
| `failed_contacts.contact` | string |  |
| `failed_contacts.error_message` | string |  |
| `failed_contacts.mail_user_id` | number |  |
| `failed_contacts.name` | string |  |
| `failed_contacts.status_code` | string |  |
| `message` | string |  |
| `validation_errors` | object |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `POST /surveys/{surveyId}/invitations/{invitationId}/sendone` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-survey-invitation.md) for the provider-specific parameters and requirements.

