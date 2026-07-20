# SmartSurvey: Replace Survey Export Emails

Replaces email addresses in future scheduled survey exports in SmartSurvey.

```
PUT https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/replace-survey-export-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/replace-survey-export-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "fromEmail": "ava@example.com",
  "toEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/replace-survey-export-emails', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "fromEmail": "ava@example.com",
    "toEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | The id of the survey whose exports you are accessing |
| `fromEmail` | string | yes | The email address to change from (not case-sensitive) |
| `toEmail` | string | yes | The email address to change it to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
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
| `code` | string |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `POST /surveys/{surveyId}/exports/replace-emails` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-survey-export-emails.md) for the provider-specific parameters and requirements.

