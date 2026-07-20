# Form.taxi: List Form Submissions

Retrieves form submissions from Form.taxi.

```
GET https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.taxi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/list-form-submissions?${params}`, {
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
| `formCode` | string | yes | The unique code of the form. Form.taxi shows it in the form settings. |
| `since` | string | no | Return only submissions created on or after this ISO 8601 timestamp. |
| `spam` | boolean | no | Include submissions from the spam folder when set to true. |
| `attachments` | boolean | no | Set to false to exclude file attachments from the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_box": "string",
      "_date": "2026-05-07T12:00:00.000Z",
      "_id": "string",
      "_url": "https://example.com",
      "attachments": [
        {}
      ],
      "fields": {},
      "fields_summary": {
        "html": "string",
        "markdown": "string",
        "text": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_box` | string | Folder where the submission is stored. |
| `_date` | date | Date and time of the submission. |
| `_id` | string | Unique ID of the submission. |
| `_url` | string | Direct URL of the submission in the Form.taxi panel. |
| `attachments` | array<object> | File attachments included with the submission. |
| `fields` | object | Form field values as key-value pairs. |
| `fields_summary.html` | string | HTML summary of submitted fields. |
| `fields_summary.markdown` | string | Markdown summary of submitted fields. |
| `fields_summary.text` | string | Plain-text summary of submitted fields. |

## Native endpoint

Through the native Form.taxi API, this operation is `GET /form/submissions/:formCode` (base URL `https://form.taxi/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

