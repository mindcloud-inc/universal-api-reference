# SmartSurvey: List Survey Exports

Retrieves all survey exports for a SmartSurvey survey.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-exports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-exports?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-exports?${params}`, {
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
| `surveyId` | number | yes | The id of the survey whose exports you are accessing |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_date": "2026-05-07T12:00:00.000Z",
      "file_content_type": "string",
      "file_extension": "string",
      "file_size": 1,
      "href": "string",
      "href_download": "string",
      "id": 1,
      "name": "Ava Chen",
      "requested_date": "2026-05-07T12:00:00.000Z",
      "started_date": "2026-05-07T12:00:00.000Z",
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
| `completed_date` | date |  |
| `file_content_type` | string |  |
| `file_extension` | string |  |
| `file_size` | number |  |
| `href` | string |  |
| `href_download` | string |  |
| `id` | number |  |
| `name` | string |  |
| `requested_date` | date |  |
| `started_date` | date |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/exports` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-survey-exports.md) for the provider-specific parameters and requirements.

