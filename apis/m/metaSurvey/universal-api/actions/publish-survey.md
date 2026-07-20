# MetaSurvey: Publish Survey



```
PUT https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/publish-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/publish-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/publish-survey', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | MetaSurvey survey identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "folderId": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "visibility": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | MetaSurvey survey identifier. |
| `createdAt` | date | When the survey was created. |
| `folderId` | string | Folder that owns the survey. |
| `publishedAt` | date | When the survey was published. |
| `title` | string | Survey title. |
| `visibility` | boolean | Whether the survey is visible to respondents. |

## Native endpoint

Through the native MetaSurvey API, this operation is `POST /admin/survey/:surveyId/publish` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-survey.md) for the provider-specific parameters and requirements.

