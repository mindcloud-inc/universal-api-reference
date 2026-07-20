# SmartSurvey: Get Survey Invitation

Retrieves a survey invitation from SmartSurvey.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-invitation?connectionId=$CONNECTION_ID&surveyId=1&invitationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "invitationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-invitation?${params}`, {
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
| `surveyId` | number | yes | The survey id whose Invitation you are querying |
| `invitationId` | number | yes | The invitation id that you are querying |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_count": 1,
      "contact_list_id": 1,
      "date_created": "2026-05-07T12:00:00.000Z",
      "date_sent": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "id": 1,
      "link_id": 1,
      "message_body": "string",
      "message_sender": "string",
      "message_sender_name": "Ava Chen",
      "message_subject": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_count` | number |  |
| `contact_list_id` | number |  |
| `date_created` | date |  |
| `date_sent` | date |  |
| `href` | string |  |
| `id` | number |  |
| `link_id` | number |  |
| `message_body` | string |  |
| `message_sender` | string |  |
| `message_sender_name` | string |  |
| `message_subject` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/invitations/{invitationId}` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-invitation.md) for the provider-specific parameters and requirements.

