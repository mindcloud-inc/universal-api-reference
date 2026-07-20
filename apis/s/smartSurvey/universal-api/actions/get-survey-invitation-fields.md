# SmartSurvey: Get Survey Invitation Fields

Retrieves custom fields for a SmartSurvey invitation.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-invitation-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-invitation-fields?connectionId=$CONNECTION_ID&surveyId=1&invitationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "invitationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-invitation-fields?${params}`, {
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
| `invitationId` | number | yes | The invitation whose fields you are querying |

## Response

```json
{
  "success": true,
  "data": [
    {
      "help_text": "string",
      "key": "string",
      "label": "string",
      "required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `help_text` | string |  |
| `key` | string |  |
| `label` | string |  |
| `required` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/invitations/{invitationId}/fields` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-invitation-fields.md) for the provider-specific parameters and requirements.

