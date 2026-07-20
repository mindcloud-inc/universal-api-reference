# SmartSurvey: Create Survey

Creates a new survey in SmartSurvey.

```
POST https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/create-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | The title for the new survey |
| `languageId` | number | no | The language id for the new survey |
| `themeId` | number | no | The theme id for the new survey |
| `folderId` | number | no | The folder id for the new survey |

## Response

```json
{
  "success": true,
  "data": [
    {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_created` | date |  |
| `date_modified` | date |  |
| `href` | string |  |
| `href_links` | string |  |
| `href_responses` | string |  |
| `id` | number |  |
| `nickname` | string |  |
| `responses` | number |  |
| `status` | string |  |
| `survey_url` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `POST /surveys` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey.md) for the provider-specific parameters and requirements.

