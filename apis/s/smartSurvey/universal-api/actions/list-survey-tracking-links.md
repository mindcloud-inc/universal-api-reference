# SmartSurvey: List Survey Tracking Links

Retrieves tracking links for a SmartSurvey survey.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-tracking-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-tracking-links?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-tracking-links?${params}`, {
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
| `responses` | number |  |
| `status` | string |  |
| `survey_url` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/links` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-survey-tracking-links.md) for the provider-specific parameters and requirements.

