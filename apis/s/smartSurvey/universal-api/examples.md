# SmartSurvey Universal API Examples

These examples use the MindCloud API key and SmartSurvey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Surveys

Retrieves all surveys in your SmartSurvey account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-surveys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [List Surveys action reference](actions/list-surveys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartSurvey/latest/actions/list-surveys).

## Close Survey

Closes a survey and its tracking links in SmartSurvey.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/close-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/close-survey', {
  method: 'PUT',
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

Example response:

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

See the full [Close Survey action reference](actions/close-survey.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartSurvey/latest/actions/close-survey).
