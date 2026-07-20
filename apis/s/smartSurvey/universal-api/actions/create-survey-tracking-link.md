# SmartSurvey: Create Survey Tracking Link

Creates a new survey tracking link in SmartSurvey.

```
POST https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey-tracking-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey-tracking-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey-tracking-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | The survey id where you want to insert the new collector |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | An optional title for the collector |
| `type` | number | no | The type of collector to create |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_closed": "2026-05-07T12:00:00.000Z",
      "date_created": "2026-05-07T12:00:00.000Z",
      "date_modified": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "id": 1,
      "properties": {},
      "responses": 1,
      "status": "string",
      "survey_url": "https://example.com",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_closed` | date |  |
| `date_created` | date |  |
| `date_modified` | date |  |
| `href` | string |  |
| `id` | number |  |
| `properties` | object |  |
| `responses` | number |  |
| `status` | string |  |
| `survey_url` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `POST /surveys/{surveyId}/links` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey-tracking-link.md) for the provider-specific parameters and requirements.

