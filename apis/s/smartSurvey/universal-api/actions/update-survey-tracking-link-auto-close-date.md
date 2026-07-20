# SmartSurvey: Update Survey Tracking Link Auto Close Date

Updates a survey tracking link auto-close date in SmartSurvey.

```
PUT https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/update-survey-tracking-link-auto-close-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/update-survey-tracking-link-auto-close-date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/update-survey-tracking-link-auto-close-date', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | The survey id whose links you are updating |
| `id` | number | yes | The tracking link id that you are updating the auto close date for |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `value` | number | no | The timestamp that you want to use for the new auto close date expressed as Unix Timestamp e.g. seconds from 01-01-1970. If it is not passed, the auto close is disabled. |

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

Through the native SmartSurvey API, this operation is `PATCH /surveys/{surveyId}/links/{id}/autoclosedate` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-survey-tracking-link-auto-close-date.md) for the provider-specific parameters and requirements.

