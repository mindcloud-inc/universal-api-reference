# Startquestion Universal API Examples

These examples use the MindCloud API key and Startquestion connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Surveys

Retrieves surveys from Startquestion.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-surveys?${params}`, {
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
      "action_after_answer": 1,
      "anonymous": 1,
      "answers_count": 1,
      "answers_limit": 1,
      "archive": 1,
      "autostart_date": "2026-05-07T12:00:00.000Z",
      "comments": 1,
      "date_created": "2026-05-07T12:00:00.000Z",
      "date_end": "2026-05-07T12:00:00.000Z",
      "date_modified": "2026-05-07T12:00:00.000Z",
      "date_published": "2026-05-07T12:00:00.000Z",
      "email_notification": 1,
      "expiration_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "internal_title": "string",
      "lang_code": "string",
      "many_answers_from_cookie": 1,
      "partial_answers": 1,
      "password": "string",
      "personal_data": 1,
      "progress_bar": 1,
      "public_results": 1,
      "question_numbers": 1,
      "redirection": "https://example.com",
      "reversible": 1,
      "search_engines": 1,
      "security_level": 1,
      "social_media": 1,
      "status": 1,
      "thank_you_text": "string",
      "title": "string",
      "type": 1,
      "url_title": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Surveys action reference](actions/list-surveys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/startquestion/latest/actions/list-surveys).

## Add Respondent to Survey

Adds a respondent to a Startquestion survey.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/add-respondent-to-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/add-respondent-to-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "contactId": 1
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
      "id_respondent": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Respondent to Survey action reference](actions/add-respondent-to-survey.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/startquestion/latest/actions/add-respondent-to-survey).
