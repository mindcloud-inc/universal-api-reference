# Startquestion: List Surveys

Retrieves surveys from Startquestion.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_after_answer` | number | Post-answer action code. |
| `anonymous` | number | Anonymous mode flag. |
| `answers_count` | number | Number of collected answers. |
| `answers_limit` | number | Survey answer limit. |
| `archive` | number | Archive state flag. |
| `autostart_date` | date | Autostart date, when configured. |
| `comments` | number | Comments enabled flag. |
| `date_created` | date | Survey creation timestamp. |
| `date_end` | date | Survey end timestamp, when configured. |
| `date_modified` | date | Last modification timestamp. |
| `date_published` | date | Survey publish timestamp, when available. |
| `email_notification` | number | Email notification flag. |
| `expiration_date` | date | Expiration date, when configured. |
| `id` | number | Survey identifier. |
| `internal_title` | string | Internal survey title. |
| `lang_code` | string | Survey language code. |
| `many_answers_from_cookie` | number | Multiple answers from one browser flag. |
| `partial_answers` | number | Partial answers flag. |
| `password` | string | Survey password when configured. |
| `personal_data` | number | Provider personal data mode flag. |
| `progress_bar` | number | Progress bar flag. |
| `public_results` | number | Public results visibility flag. |
| `question_numbers` | number | Question numbering flag. |
| `redirection` | string | Redirection URL after completion. |
| `reversible` | number | Back navigation flag. |
| `search_engines` | number | Search engine indexing flag. |
| `security_level` | number | Provider security level code. |
| `social_media` | number | Social media sharing flag. |
| `status` | number | Provider status code. |
| `thank_you_text` | string | Thank-you message shown after submission. |
| `title` | string | Survey title shown to respondents. |
| `type` | number | Provider survey type code. |
| `url_title` | string | URL-friendly survey title. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /surveys` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

