# SmartSurvey: List Survey Invitation Responses

Retrieves responses for a SmartSurvey invitation.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-invitation-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-invitation-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1&invitationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "surveyId": "1",
  "invitationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-invitation-responses?${params}`, {
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
| `invitationId` | number | yes | The invitation id whose responses you are querying |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | number | no | Filter responses by status. Possible values: 0=All, 1=Sent, 2=Queued, 3=Completed, 4=Pending, 5=Failed, 6=Opened, 7=Viewed, 8=OptedOut, 9=Deleted |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anon": true,
      "bounced": true,
      "email": "ava@example.com",
      "ended_survey": "2026-05-07T12:00:00.000Z",
      "failed": true,
      "failure_reason": "string",
      "id": 1,
      "ip_address": "string",
      "name": "Ava Chen",
      "opened": true,
      "opted_out": true,
      "reminder_sent": true,
      "responded": true,
      "response_id": 1,
      "sent": true,
      "started_survey": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "status_code": "string",
      "viewed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anon` | boolean |  |
| `bounced` | boolean |  |
| `email` | string |  |
| `ended_survey` | date |  |
| `failed` | boolean |  |
| `failure_reason` | string |  |
| `id` | number |  |
| `ip_address` | string |  |
| `name` | string |  |
| `opened` | boolean |  |
| `opted_out` | boolean |  |
| `reminder_sent` | boolean |  |
| `responded` | boolean |  |
| `response_id` | number |  |
| `sent` | boolean |  |
| `started_survey` | date |  |
| `status` | string |  |
| `status_code` | string |  |
| `viewed` | boolean |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/invitations/{invitationId}/list` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-survey-invitation-responses.md) for the provider-specific parameters and requirements.

