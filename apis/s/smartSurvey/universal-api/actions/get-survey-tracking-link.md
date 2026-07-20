# SmartSurvey: Get Survey Tracking Link

Retrieves a survey tracking link from SmartSurvey.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-tracking-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-tracking-link?connectionId=$CONNECTION_ID&surveyId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-tracking-link?${params}`, {
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
| `surveyId` | number | yes | The survey id whose links you are querying |
| `id` | number | yes | The tracking link id that you are querying |

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

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/links/{id}` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-tracking-link.md) for the provider-specific parameters and requirements.

