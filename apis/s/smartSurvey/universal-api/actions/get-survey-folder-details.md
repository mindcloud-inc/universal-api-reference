# SmartSurvey: Get Survey Folder Details

Retrieves a survey folder with its surveys from SmartSurvey.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-folder-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-folder-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-folder-details?${params}`, {
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
| `id` | number | yes | The id of the folder to get details for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string",
      "id": 1,
      "surveys": {
        "date_created": "2026-05-07T12:00:00.000Z",
        "date_modified": "2026-05-07T12:00:00.000Z",
        "href": "string",
        "href_links": "https://example.com",
        "href_responses": "string",
        "id": 1,
        "nickname": "Ava Chen",
        "responses": 1,
        "status": "string",
        "survey_url": "https://example.com",
        "title": "string",
        "type": "string"
      },
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
| `href` | string |  |
| `id` | number |  |
| `surveys` | array<object> |  |
| `surveys.date_created` | date |  |
| `surveys.date_modified` | date |  |
| `surveys.href` | string |  |
| `surveys.href_links` | string |  |
| `surveys.href_responses` | string |  |
| `surveys.id` | number |  |
| `surveys.nickname` | string |  |
| `surveys.responses` | number |  |
| `surveys.status` | string |  |
| `surveys.survey_url` | string |  |
| `surveys.title` | string |  |
| `surveys.type` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveyfolders/{id}/detailed` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-folder-details.md) for the provider-specific parameters and requirements.

